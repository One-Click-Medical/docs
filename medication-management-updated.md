# Guide utilisateur : Gestion des médicaments

## Introduction

Le module de gestion des médicaments de OneClickMedical permet aux professionnels de santé de gérer une base de données complète de médicaments, qui peut être utilisée pour créer des ordonnances et suivre les traitements des patients. Ce guide explique en détail comment utiliser toutes les fonctionnalités de ce module.

### Rôles et accès

Les rôles suivants ont accès au module de gestion des médicaments :

- **Infirmier** : Peut consulter, rechercher et utiliser les médicaments dans les soins
- **Médecin** : Peut consulter, rechercher et utiliser les médicaments dans les prescriptions
- **Super Médecin** : Peut consulter, rechercher, créer, modifier et désactiver/réactiver des médicaments
- **Admin** : Accès complet incluant l'importation et la suppression de médicaments
- **Super Admin** : Accès complet avec droits étendus sur la gestion du système

## Table des matières

1. [Consulter la liste des médicaments](#1-consulter-la-liste-des-médicaments)
2. [Rechercher des médicaments](#2-rechercher-des-médicaments)
3. [Consulter les détails d'un médicament](#3-consulter-les-détails-dun-médicament)
4. [Ajouter un nouveau médicament](#4-ajouter-un-nouveau-médicament)
5. [Modifier un médicament existant](#5-modifier-un-médicament-existant)
6. [Désactiver et réactiver un médicament](#6-désactiver-et-réactiver-un-médicament)
7. [Importer des médicaments](#7-importer-des-médicaments)
8. [Utiliser les médicaments dans les prescriptions](#8-utiliser-les-médicaments-dans-les-prescriptions)

## 1. Consulter la liste des médicaments

La page principale du module de gestion des médicaments présente la liste de tous les médicaments disponibles dans le système.

**Pour accéder à cette page :**
1. Connectez-vous à votre compte OneClickMedical
2. Dans le menu latéral, cliquez sur "Médicaments"

**Fonctionnalités de la liste :**
- Pagination pour naviguer entre les pages
- Affichage du nombre total de médicaments
- Indication visuelle des médicaments actifs et inactifs
- Boutons d'action discrets pour consulter, modifier et désactiver/réactiver un médicament
- Bouton "Ajouter un médicament" pour créer une nouvelle entrée

**Navigation :**
- Un fil d'Ariane (breadcrumb) est disponible en haut de la page pour faciliter la navigation
- Les éléments interactifs sont clairement identifiables grâce au curseur pointer

## 2. Rechercher des médicaments

La fonction de recherche vous permet de trouver rapidement des médicaments spécifiques dans la base de données.

**Pour rechercher un médicament :**
1. Sur la page principale des médicaments, utilisez la barre de recherche en haut
2. Saisissez un terme de recherche (minimum 2 caractères)
3. La recherche s'effectue automatiquement et affiche les résultats correspondants
4. Le champ de recherche reçoit automatiquement le focus à l'ouverture de la page

**Critères de recherche :**
- Nom commercial du médicament
- Nom générique/principe actif
- Forme galénique

**Filtres disponibles :**
- Afficher/masquer les médicaments inactifs (bascule en haut de la liste)

## 3. Consulter les détails d'un médicament

Pour voir toutes les informations concernant un médicament spécifique :

1. Dans la liste des médicaments, cliquez sur le nom du médicament
2. La page de détails s'affiche avec toutes les informations disponibles
3. Un fil d'Ariane en haut de la page permet de naviguer facilement

**Informations affichées :**
- **Informations générales**
  - Nom du médicament
  - Forme et dosage
  - Statut actif/inactif
  - Indication si une prescription est requise
  - Informations sur le remboursement (taux de remboursement)

- **Détails cliniques**
  - Description complète
  - Contre-indications
  - Effets secondaires
  - Interactions médicamenteuses
  - Catégories (tags affichés sous forme de badges)

- **Informations administratives**
  - Date de création
  - Date de dernière mise à jour

**Actions disponibles :**
- Retour à la liste (bouton en haut)
- Modifier (bouton d'action, disponible selon les droits d'accès)
- Activer/Désactiver (bouton d'action, disponible selon les droits d'accès)

## 4. Ajouter un nouveau médicament

> **Note :** Cette fonctionnalité est accessible uniquement aux utilisateurs ayant les rôles Super Médecin, Admin ou Super Admin.

Pour ajouter un nouveau médicament dans la base de données :

1. Sur la page principale des médicaments, cliquez sur le bouton "Ajouter un médicament"
2. Remplissez le formulaire avec les informations requises
3. Les champs obligatoires sont marqués d'un astérisque (*)
4. Cliquez sur "Enregistrer" pour ajouter le médicament

**Sections du formulaire :**
- **Informations générales**
  - Nom du médicament*
  - Forme galénique*
  - Dosage/Concentration*
  - Prescription requise (oui/non)
  - Statut actif (activé par défaut)

- **Détails cliniques**
  - Description
  - Contre-indications
  - Effets secondaires
  - Interactions médicamenteuses
  - Catégories (entrées séparées par des virgules)

- **Remboursement**
  - Remboursable (oui/non)
  - Taux de remboursement (%)

## 5. Modifier un médicament existant

> **Note :** Cette fonctionnalité est accessible uniquement aux utilisateurs ayant les rôles Super Médecin, Admin ou Super Admin.

Pour modifier les informations d'un médicament :

1. Depuis la liste des médicaments ou la page de détails, cliquez sur le bouton "Modifier"
2. Le formulaire d'édition s'ouvre, pré-rempli avec les informations actuelles
3. Modifiez les champs nécessaires
4. Cliquez sur "Enregistrer les modifications" pour appliquer les changements

**Remarque :** L'interface de modification est similaire à celle d'ajout d'un nouveau médicament, avec les mêmes sections et champs.

## 6. Désactiver et réactiver un médicament

> **Note :** Cette fonctionnalité est accessible uniquement aux utilisateurs ayant les rôles Super Médecin, Admin ou Super Admin.

Pour désactiver un médicament sans le supprimer définitivement :

1. Dans la liste des médicaments ou sur la page de détails, cliquez sur le bouton d'activation/désactivation
2. Confirmez votre action dans la boîte de dialogue qui apparaît
3. Un message de confirmation s'affiche brièvement
4. Le médicament sera marqué comme inactif et apparaîtra grisé dans la liste

Pour réactiver un médicament désactivé :

1. Assurez-vous que les médicaments inactifs sont visibles (utilisez le filtre "Afficher les médicaments inactifs")
2. Cliquez sur le bouton d'activation pour le médicament inactif
3. Un message de confirmation s'affiche brièvement
4. Le médicament sera à nouveau marqué comme actif

**Remarque importante :** Les médicaments inactifs n'apparaissent pas dans les listes de sélection lors de la création d'ordonnances.

## 7. Importer des médicaments

> **Note :** Cette fonctionnalité est accessible uniquement aux utilisateurs ayant les rôles Admin ou Super Admin.

Le système permet d'importer des médicaments en masse à partir de fichiers CSV ou JSON.

**Pour accéder à la page d'importation :**
1. Sur la page principale des médicaments, cliquez sur "Importer des médicaments"
2. Choisissez le type d'importation souhaité (CSV ou JSON)

**Importation CSV :**
1. Sélectionnez le fichier CSV contenant vos données
2. Spécifiez le délimiteur utilisé dans le fichier (virgule, point-virgule, etc.)
3. Définissez le nombre maximum d'éléments à importer (optionnel)
4. Cliquez sur "Importer" pour lancer le processus

**Importation JSON :**
1. Sélectionnez le fichier JSON contenant vos données
2. Définissez le nombre maximum d'éléments à importer (optionnel)
3. Cliquez sur "Importer" pour lancer le processus

**Format des fichiers d'importation :**
- CSV : le fichier doit contenir une ligne d'en-tête avec les noms des champs
- JSON : le fichier doit contenir un tableau d'objets avec les propriétés des médicaments

## 8. Utiliser les médicaments dans les prescriptions

Les médicaments enregistrés dans le système peuvent être facilement ajoutés aux prescriptions des patients.

**Pour ajouter un médicament à une prescription :**
1. Dans le module de prescriptions, créez une nouvelle ordonnance ou modifiez une existante
2. Dans la section "Médicaments", utilisez le champ de recherche pour trouver un médicament
3. Commencez à taper le nom du médicament pour voir apparaître les suggestions en temps réel
4. Utilisez les flèches du clavier pour naviguer dans les résultats et appuyez sur Entrée pour sélectionner
5. Complétez les informations de prescription (dosage, fréquence, durée, instructions)
6. Cliquez sur "Ajouter à l'ordonnance" pour inclure le médicament

**Modifier un médicament dans une prescription :**
1. Dans la liste des médicaments prescrits, cliquez sur le bouton de modification
2. Modifiez les champs nécessaires
3. Cliquez sur "Enregistrer les modifications"

**Supprimer un médicament d'une prescription :**
1. Dans la liste des médicaments prescrits, cliquez sur l'icône de suppression
2. Le médicament est immédiatement retiré de la liste

**Interactions médicamenteuses :**
Le système affiche automatiquement un avertissement concernant les interactions médicamenteuses potentielles lorsque plusieurs médicaments sont ajoutés à une même ordonnance.

## Assistance supplémentaire

Si vous avez des questions ou rencontrez des difficultés avec le module de gestion des médicaments, veuillez contacter le support technique de OneClickMedical à l'adresse support@oneclickmedical.com ou par téléphone au +229 01609348.
