# Guide d'utilisation : Validation des soins réalisés

## Introduction

La fonctionnalité "Validation des soins réalisés" permet aux infirmiers de marquer les médicaments comme administrés lors de leurs interventions auprès des patients. Le système prend en charge les administrations multiples pour les traitements qui s'étendent sur plusieurs jours, avec un suivi visuel de la progression. Cette documentation présente les étapes d'utilisation et de navigation pour cette nouvelle fonctionnalité.

## Profils concernés

- **Infirmier** : Validation de l'administration des médicaments
- **Médecin/Super-médecin** : Consultation de l'historique des administrations
- **Patient** : Consultation de l'historique des soins reçus
- **Admin/Super-admin** : Supervision et gestion des validations

## Navigation et utilisation

### Étape 1 : Accéder aux prescriptions

1. Connectez-vous à votre compte OneClickMedical avec vos identifiants
2. Dans le menu latéral, cliquez sur l'onglet **Prescriptions**
3. Consultez la liste des prescriptions actives 
4. Cliquez sur la prescription pour laquelle vous souhaitez valider l'administration d'un médicament

### Étape 2 : Visualiser les médicaments prescrits

La page détaillée de la prescription affiche :
- Informations générales sur la prescription
- Liste des médicaments prescrits
- Options de validation des soins (visible uniquement pour les infirmiers et rôles supérieurs)

### Étape 3 : Valider l'administration d'un médicament (rôle Infirmier)

1. Dans la section "Médicaments prescrits", localisez le médicament administré
2. Observez la **barre de progression** qui indique le nombre d'administrations déjà effectuées (X / Y)
3. Cliquez sur le bouton **Valider le soin** à côté du médicament concerné
4. Dans le formulaire qui s'affiche :
   - Saisissez la **quantité administrée** (par défaut : quantité prescrite)
   - Ajoutez des **notes** si nécessaire (ex: réaction du patient, problèmes rencontrés)
5. Cliquez sur **Valider l'administration**
6. Une notification de confirmation s'affiche
7. L'historique des administrations et la barre de progression se mettent à jour automatiquement

### Étape 4 : Comprendre le suivi de progression

Le système calcule automatiquement le nombre total d'administrations requises en fonction de :
- **Fréquence** du médicament (combien de fois par jour/semaine/mois)
- **Période** d'administration (quotidien, hebdomadaire, mensuel, au besoin)
- **Durée du traitement** en jours

Pour chaque médicament, vous verrez :
- Une barre de progression colorée indiquant l'avancement du traitement
- Un compteur d'administrations (ex: "3 / 10")
- Le nombre d'administrations restantes

La prescription ne sera marquée comme "Terminée" que lorsque **tous** les médicaments auront reçu **toutes** les administrations requises.

### Étape 5 : Consulter l'historique des administrations

1. L'historique spécifique à chaque médicament est visible directement sous le médicament concerné
2. L'historique complet des administrations pour toute la prescription est disponible en bas de la page
3. Pour chaque administration, vous pouvez consulter :
   - Le nom du médicament
   - La date et l'heure d'administration
   - L'infirmier ayant effectué l'administration
   - La quantité administrée
   - Les notes éventuelles

### Étape 5 : Suivi des prescriptions complètement administrées

1. Lorsque tous les médicaments d'une prescription ont été administrés au moins une fois, le statut de la prescription passe automatiquement à "Complétée"
2. Ce changement de statut est visible sur la page de détail de la prescription
3. La prescription reste consultable mais ne permet plus de nouvelles validations

## Bonnes pratiques

- Validez l'administration immédiatement après avoir administré le médicament
- Ajoutez des notes détaillées en cas d'effets secondaires ou de réactions particulières
- Vérifiez régulièrement l'historique pour assurer un suivi optimal du traitement

## Résolution des problèmes courants

| Problème | Solution |
|---------|----------|
| Le bouton "Valider le soin" n'est pas visible | Vérifiez que vous êtes connecté avec un compte Infirmier et que la prescription est active |
| Erreur lors de la validation | Vérifiez votre connexion internet et réessayez. Si le problème persiste, contactez l'administrateur |
| L'historique ne se met pas à jour | Cliquez sur le bouton "Actualiser" en bas de l'historique des administrations |

## Notes importantes

- Seules les prescriptions avec le statut "Active" peuvent faire l'objet d'une validation de soins
- Les infirmiers ne peuvent pas modifier ou supprimer une validation déjà enregistrée
- Toutes les validations sont horodatées et traçables pour des raisons de sécurité et d'audit

---

Cette fonctionnalité s'inscrit dans la démarche globale de OneClickMedical visant à améliorer le suivi des soins et la communication entre les différents professionnels de santé impliqués dans le parcours du patient.
