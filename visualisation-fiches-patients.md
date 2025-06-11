# Guide d'utilisation et documentation technique : Système de visualisation des fiches patients

## Introduction

Ce document explique le fonctionnement du système de visualisation des fiches patients implémenté dans OneClickMedical, avec un focus particulier sur la page de détail patient et l'implémentation technique des graphiques de données médicales.

## Table des matières

1. [Vue d'ensemble](#vue-densemble)
2. [Page de détail patient](#page-de-détail-patient)
3. [Page d'historique des consultations](#page-dhistorique-des-consultations)
4. [Implémentation technique des graphiques](#implémentation-technique-des-graphiques)
5. [Flux de données](#flux-de-données)
6. [Contrôle d'accès](#contrôle-daccès)
7. [Fonctionnalités futures](#fonctionnalités-futures)

## Vue d'ensemble

Le système de visualisation des fiches patients permet aux utilisateurs autorisés (médecins, infirmiers, super-médecins et administrateurs) de consulter les informations complètes d'un patient, incluant :

- Données personnelles et démographiques
- Informations médicales importantes (groupe sanguin, allergies, antécédents)
- Évolution des paramètres vitaux et biométriques au fil du temps
- Représentations graphiques des données médicales
- Tableau récapitulatif des dernières mesures

Cette fonctionnalité s'inscrit dans la stratégie globale de OneClickMedical de fournir un accès centralisé et sécurisé aux informations médicales des patients.

## Page de détail patient

### Structure et organisation

La page de détail patient est divisée en trois sections principales :

1. **Informations personnelles du patient**
   - Photo de profil / Avatar (avec fallback sur les initiales du patient si aucun avatar n'est disponible)
   - Nom, prénom et âge
   - Coordonnées (email, téléphone, adresse)
   - Groupe sanguin
   - Allergies connues
   - Antécédents médicaux

2. **Évolution médicale**
   - Graphiques interactifs montrant l'évolution de différents paramètres :
     - Poids (kg)
     - Température (°C)
     - Fréquence cardiaque (bpm) et glycémie (mg/dL)
   - Tableau récapitulatif des dernières mesures

3. **Actions disponibles**
   - Ajouter une consultation (ouvre automatiquement le modal d'ajout avec le patient présélectionné)
   - Modifier les informations
   - Voir l'historique (redirige vers la page d'historique des consultations)
   - Supprimer le patient (réservé aux utilisateurs autorisés)

### Navigation

Pour accéder à la page de détail d'un patient :
1. Connectez-vous à l'application
2. Accédez au tableau de bord
3. Dans la section des patients, cliquez sur le bouton "VOIR PLUS" d'une carte patient
4. Vous serez redirigé vers la page de détail du patient sélectionné

Un bouton de retour en haut de page permet de revenir à la liste des patients.

## Page d'historique des consultations

### Structure et organisation

La page d'historique des consultations offre une vue chronologique des consultations passées du patient. Elle est structurée comme suit :

1. **En-tête**
   - Bouton de retour à la page précédente
   - Titre "HISTORIQUE DES CONSULTATIONS"

2. **Information du patient**
   - Photo/Avatar du patient (avec fallback sur les initiales si aucun avatar n'est disponible)
   - Nom, prénom du patient
   - Email du patient
   - Bouton "Ajouter une consultation" qui redirige vers la page des rendez-vous avec le patient présélectionné

3. **Liste des consultations**
   - Triées par ordre chronologique inverse (la plus récente en premier)
   - Pour chaque consultation :
     - Titre et date de la consultation
     - Description/contenu de la consultation
     - Données médicales relevées (si disponibles)
     - Type de rapport
     - Référence à une prescription (si applicable)
     - Information sur le médecin ayant réalisé la consultation

### Navigation

Pour accéder à la page d'historique des consultations :
1. Accédez à la page de détail d'un patient
2. Cliquez sur le bouton "Voir l'historique" dans la section des actions
3. Vous serez redirigé vers la page d'historique des consultations du patient

### Fonctionnalités

- **Visualisation chronologique** : Consultations affichées de la plus récente à la plus ancienne
- **Ajout direct** : Possibilité d'ajouter une nouvelle consultation depuis cette page
- **Données contextuelles** : Chaque consultation affiche les données médicales relevées lors de celle-ci
- **Navigation intuitive** : Retour facile à la page de détail patient

## Implémentation technique des graphiques

Les graphiques de données médicales sont implémentés à l'aide de la bibliothèque [Recharts](https://recharts.org/), un composant de graphiques redéfinissable construit avec React et D3.

### Structure des composants graphiques

Tous les graphiques utilisent le schéma suivant :

1. Un conteneur responsive (`ResponsiveContainer`)
2. Un type de graphique spécifique (`LineChart`)
3. Des composants pour les axes (`XAxis`, `YAxis`)
4. Une grille (`CartesianGrid`)
5. Des infobulles (`Tooltip`)
6. Une légende (`Legend`)
7. Les séries de données (`Line`)

### Exemple d'implémentation d'un graphique de poids

```jsx
<ResponsiveContainer width="100%" height={250}>
  <LineChart data={medicalData}>
    <CartesianGrid strokeDasharray="3 3" />
    <XAxis dataKey="date" />
    <YAxis domain={['auto', 'auto']} />
    <Tooltip />
    <Legend />
    <Line 
      type="monotone" 
      dataKey="poids" 
      name="Poids (kg)" 
      stroke="#9C0DA3" 
      strokeWidth={2} 
      activeDot={{ r: 8 }} 
    />
  </LineChart>
</ResponsiveContainer>
```

### Particularités techniques des graphiques

#### 1. Graphique du poids

- Type : `LineChart` (graphique linéaire)
- Axe Y : Échelle automatique (`domain={['auto', 'auto']}`)
- Couleur : Violet OneClickMedical (`#9C0DA3`)

#### 2. Graphique de la température

- Type : `LineChart`
- Axe Y : Commence à 36°C (`domain={[36, 'auto']}`)
- Couleur : Orange (`#FF5733`)

#### 3. Graphique combiné fréquence cardiaque et glycémie

- Type : `LineChart` avec deux séries de données
- Double axe Y : 
  - Axe gauche : Fréquence cardiaque
  - Axe droit : Glycémie
- Couleurs :
  - Fréquence cardiaque : Violet (`#8884d8`)
  - Glycémie : Vert (`#82ca9d`)

Ce graphique utilise la fonctionnalité de double axe Y de Recharts pour afficher deux mesures avec des échelles différentes sur le même graphique.

## Flux de données

### Fonctionnement du bouton "Ajouter une consultation"

Le bouton "Ajouter une consultation" présent sur la page de détail patient et la page d'historique implémente un flux particulier :

1. Lorsque l'utilisateur clique sur ce bouton, il est redirigé vers la page des rendez-vous (`/dashboard/appointments`) avec l'ID du patient transmis en paramètre d'URL : `/dashboard/appointments?patientId=XXX`

2. La page des rendez-vous détecte la présence du paramètre `patientId` dans l'URL via `useSearchParams` et déclenche automatiquement l'ouverture du modal d'ajout de rendez-vous

3. Le modal d'ajout de rendez-vous reçoit l'ID du patient via la prop `initialPatientId` et présélectionne automatiquement le patient dans le formulaire

Ce mécanisme permet une expérience utilisateur fluide pour créer rapidement une consultation pour un patient spécifique, tout en réutilisant le modal existant d'ajout de rendez-vous.

```javascript
// Extrait du code de la page des rendez-vous
useEffect(() => {
  // Vérifier s'il y a un patientId dans l'URL pour ouvrir automatiquement le modal
  const patientId = searchParams.get('patientId');
  if (patientId) {
    setPreselectedPatientId(patientId);
    setIsCreateModalOpen(true);
  }
}, [searchParams]);
```

### Sources de données

Les données affichées sur la page de détail patient proviennent de deux endpoints API principaux :

1. `/users/patient/:id` - Informations personnelles du patient
2. `/medical-reports/patient/:id` - Rapports médicaux contenant les données de suivi

### Traitement des données

Le processus de traitement des données se déroule comme suit :

1. L'ID du patient est récupéré depuis les paramètres de l'URL
2. Les informations du patient sont chargées via l'API
3. Les rapports médicaux sont récupérés et transformés en un format adapté aux graphiques
4. Si aucune donnée médicale n'est disponible, des données de démonstration sont générées

```javascript
// Exemple de transformation des données pour les graphiques
const formattedData = patientReports
  .filter(report => report.medicalData)
  .map(report => ({
    date: new Date(report.createdAt).toLocaleDateString('fr-FR'),
    poids: report.medicalData?.poids || 0,
    taille: report.medicalData?.taille || 0,
    temperature: report.medicalData?.temperature || 0,
    // autres données...
  }));
```

## Contrôle d'accès

La page de détail patient est protégée par un système de contrôle d'accès basé sur les rôles. Seuls les utilisateurs ayant les rôles suivants peuvent accéder à cette page :

- MEDECIN
- INFIRMIER
- SUPER_MEDECIN
- ADMIN
- SUPER_ADMIN

Cette protection est mise en œuvre via le HOC (Higher-Order Component) `withRoleProtection` qui vérifie le rôle de l'utilisateur avant d'afficher la page.

---

Ce document a été créé pour aider les utilisateurs et les développeurs à comprendre le fonctionnement du système de visualisation des fiches patients dans OneClickMedical. Pour toute question ou suggestion, veuillez contacter l'équipe technique.
