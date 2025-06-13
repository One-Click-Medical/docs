# Guide d'utilisation - Gestion des utilisateurs

## Introduction

Ce guide détaille le processus de gestion des utilisateurs dans l'application OneClickMedical (OCM). Il est destiné aux administrateurs et super-administrateurs qui ont la responsabilité de gérer les comptes utilisateurs.

## Accès à la gestion des utilisateurs

1. Connectez-vous à l'application OCM avec vos identifiants d'administrateur ou super administrateur
2. Dans le menu de navigation latéral, cliquez sur **Utilisateurs** (si vous êtes administrateur) ou **Gestion utilisateurs** (si vous êtes super administrateur)

> **Note** : L'accès à cette fonctionnalité est réservé aux utilisateurs ayant les rôles Admin ou Super Admin.

## Fonctionnalités principales

### Visualisation des utilisateurs

L'interface principale affiche un tableau contenant tous les utilisateurs du système avec les informations suivantes :
- Nom et prénom
- Email
- Rôle (Patient, Médecin, Super Médecin, Infirmier, Admin, Super Admin)
- Statut (Actif/Inactif)
- Date de création du compte
- Actions disponibles

### Filtres et recherche

Vous pouvez filtrer la liste des utilisateurs de plusieurs façons :
- **Barre de recherche** : Recherchez un utilisateur par son nom, prénom ou email
- **Filtre par rôle** : Affichez uniquement les utilisateurs d'un rôle spécifique
- **Pagination** : Naviguez entre les différentes pages de résultats

### Création d'un nouvel utilisateur

Pour ajouter un nouvel utilisateur au système :

1. Cliquez sur le bouton **Ajouter un utilisateur** en haut à droite
2. Remplissez le formulaire avec les informations requises :
   - Email (obligatoire)
   - Mot de passe et confirmation (obligatoires)
   - Nom et prénom (obligatoires)
   - Rôle (obligatoire)
   - Numéro de téléphone (optionnel)
   - Genre (optionnel)
3. Cliquez sur **Créer l'utilisateur**

> **Note** : Le système vérifiera que l'email est unique et correctement formaté. Les mots de passe doivent contenir au minimum 8 caractères.

### Modification d'un utilisateur existant

Pour modifier les informations d'un utilisateur :

1. Localisez l'utilisateur dans la liste
2. Cliquez sur l'icône de crayon (✏️) dans la colonne Actions
3. Dans le formulaire qui s'affiche, modifiez les champs souhaités :
   - Email
   - Nom et prénom
   - Rôle
   - Numéro de téléphone
   - Genre
   - Statut (Actif/Inactif)
   - Mot de passe (optionnel - laissez vide pour conserver le mot de passe actuel)
4. Cliquez sur **Enregistrer les modifications**

### Activation/Désactivation d'un utilisateur

Pour changer le statut d'un utilisateur sans le supprimer :

1. Localisez l'utilisateur dans la liste
2. Cliquez sur l'interrupteur (toggle) dans la colonne Statut
3. Confirmez votre action dans la boîte de dialogue

> **Note** : Un utilisateur désactivé ne pourra plus se connecter à l'application mais ses données seront conservées.

### Suppression d'un utilisateur

Pour supprimer définitivement un utilisateur :

1. Localisez l'utilisateur dans la liste
2. Cliquez sur l'icône de corbeille (🗑️) dans la colonne Actions
3. Confirmez la suppression dans la boîte de dialogue

> **Attention** : La suppression d'un utilisateur est irréversible. Toutes ses données personnelles seront définitivement effacées du système.

## Bonnes pratiques

- **Rôles appropriés** : Attribuez toujours le niveau de privilège minimal nécessaire pour chaque utilisateur
- **Mots de passe** : Encouragez l'utilisation de mots de passe forts lors de la création de nouveaux comptes
- **Vérification** : Avant de supprimer un utilisateur, vérifiez qu'il n'est pas associé à des données importantes (rendez-vous, dossiers médicaux, etc.)
- **Audit** : Effectuez régulièrement un audit des comptes utilisateurs pour désactiver ceux qui ne sont plus nécessaires

## Résolution des problèmes courants

| Problème | Solution |
|---------|---------|
| Un utilisateur ne peut pas se connecter | Vérifiez que son compte est actif et que son email est correct |
| Erreur lors de la création d'utilisateur | Vérifiez que l'email n'est pas déjà utilisé et que tous les champs obligatoires sont remplis |
| Un utilisateur n'a pas accès à certaines fonctionnalités | Vérifiez que son rôle est correctement configuré |

## Assistance

Si vous rencontrez des problèmes techniques avec la gestion des utilisateurs, veuillez contacter l'équipe support OneClickMedical :
- Email : contact@ronasdev.com
- Téléphone : +229 01 60 93 48 17
