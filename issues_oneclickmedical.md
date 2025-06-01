# ✅ Issues à créer pour OneClickMedical

## Implémenter l’authentification JWT

**Description :** Permettre la connexion avec email et mot de passe via JWT

**Labels :** `auth,backend,type:feature,priority:high`


---

## Intégrer la connexion via Google (OAuth2)

**Description :** Connexion utilisateur via Google OAuth

**Labels :** `auth,backend,type:feature,priority:medium`


---

## Créer le système de rôles (RBAC)

**Description :** Définir les rôles : patient, médecin, infirmier, super médecin, super admin, admin

**Labels :** `auth,backend,type:feature,priority:high`


---

## Mise en place des guards de sécurité par rôle

**Description :** Interdire l'accès aux routes selon rôle avec NestJS guards

**Labels :** `sécurité,backend,type:feature,priority:high`


---

## Checklist de sécurité & conformité RGPD

**Description :** Documenter et vérifier les règles de sécurité à chaque étape

**Labels :** `sécurité,type:doc,priority:high`

S2

---
## Création et modification du profil utilisateur
**Description :** `photo, prénom, genre, numéro, notifications. Interface et back. `

**Labels :** `user,backend,frontend,type:feature,priority:medium`

---
## Création de créneaux de disponibilité (slots)

**Description :** Interface et back pour que les médecins définissent leurs horaires

**Labels :** `médecin,backend,frontend,type:feature,priority:high`


---

## Création d’ordonnances et prescriptions

**Description :** Ajout d’ordonnances + sélection des médicaments depuis la base

**Labels :** `médecin,carnet,type:feature,priority:high`


---

## Ajout de rapports médicaux

**Description :** Permettre au médecin d’uploader un rapport dans le carnet

**Labels :** `médecin,carnet,type:feature,priority:medium`


---

## Créer un RDV en tant que médecin pour un patient

**Description :** Le médecin peut initier un rendez-vous et l’assigner à un patient

**Labels :** `médecin,rendez-vous,frontend,backend,type:feature,priority:high`


S3
---


## Prise de rendez-vous (par body malaise)

**Description :** Patient choisit une zone → proposition de créneaux

**Labels :** `patient,frontend,type:feature,priority:high`


---

## Workflow post-création du RDV

**Description :** Notifier et gérer le cas abonné/non-abonné après la création du RDV

**Labels :** `rendez-vous,notifications,backend,type:feature,priority:medium`


---


## Feedback post-consultation

**Description :** Patient peut noter médecin et ajouter un commentaire

**Labels :** `patient,frontend,type:feature,priority:medium`


---


## Historique des consultations

**Description :** Interface avec filtres par date, médecin, statut

**Labels :** `patient,frontend,type:feature,priority:medium`


---

S4

## Accès à la base de données ou création de base de données des médicaments et intégration d’interface médical

**Description :** Accès à la base de données des médicaments et intégration d’interface médical
                    Structure table « drugs » avec nom, principe actif, posologie

**Labels :** `backend,carnet,type:feature,priority:high`


---

## Ajout dynamique des médicaments dans une ordonnance

**Description :** Recherche rapide de médicaments dans le carnet

**Labels :** `carnet,frontend,type:feature,priority:medium`


---

## Visualisation sécurisée du carnet médical par le patient

**Description :** Lecture seule, aucune option de téléchargement

**Labels :** `patient,carnet,frontend,type:feature,priority:high`


---

## Ajout d'observations dans le carnet médical

**Description :** Notes infirmières visibles par médecin et patient

**Labels :** `infirmier,carnet,backend,type:feature,priority:medium`


---

## Validation des soins réalisés

**Description :** Marquer les soins comme effectués par l'infirmier

**Labels :** `infirmier,carnet,type:feature,priority:low`


---

S5

## Visualisation des feedbacks par les médecins

**Description :** Les médecins doivent pouvoir consulter les feedbacks laissés par leurs patients après les consultations. Les administrateurs doivent également pouvoir visualiser les feedbacks de tous les médecins via une interface dédiée.

**Fonctionnalités attendues :**
- Interface pour que les médecins puissent voir leurs feedbacks (note moyenne, liste pagination)
- Vue détaillée d'un feedback avec possibilité de voir les commentaires complets
- Interface administrateur pour consulter les feedbacks de tous les médecins
- Accès depuis le menu de navigation latéral

**Labels :** `medecin,admin,frontend,backend,type:feature,priority:medium`


---

## Intégration de Socket.io pour chat temps réel

**Description :** Patient ↔ médecin, message instantané, notifications socket

**Labels :** `chat,frontend,backend,type:feature,priority:high`


---

## Implémentation du chatbot OCM-AI Assistant

**Description :** Assistant pour aider à la prise de RDV ou infos basiques

**Labels :** `assistant,IA,frontend,type:feature,priority:medium`


---

## Notifications socket lors des changements de statut de RDV

**Description :** Ex: pending → confirmed, annulé, etc.

**Labels :** `notifications,socket,backend,type:feature,priority:high`


---

## Envoi de notifications par email

**Description :** Ex: nouveau RDV, rappel, ordonnance disponible

**Labels :** `notifications,email,backend,type:feature,priority:medium`


---
S6

## Création d’événements (campagnes, sessions, etc.)

**Description :** Interface + module agenda médecin/infirmier/patient

**Labels :** `événements,frontend,backend,type:feature,priority:medium`


---

## Tableau de bord dynamique selon rôle

**Description :** Indicateurs clés, résumé activité, RDV à venir

**Labels :** `dashboard,frontend,type:feature,priority:medium`


---

## Initialiser la base de données avec Prisma

**Description :** Setup du schéma, migrations et seed de données

**Labels :** `backend,base,type:setup,priority:medium`


---


## Fichier .env.example + instructions d’installation

**Description :** Créer un modèle d'environnement clair

**Labels :** `setup,doc,type:config,priority:low`


---

## Créer un README pro avec étapes de démarrage

**Description :** Documentation de lancement projet

**Labels :** `doc,type:doc,priority:medium`


---

## Mettre en place une procédure de déploiement

**Description :** Déploiement sur Railway, Vercel ou autre

**Labels :** `devops,backend,type:setup,priority:low`


---

## Vue globale sur tous les patients et consultations

**Description :** Super-médecin accède à toutes les données

**Labels :** `super-médecin,backend,frontend,type:feature,priority:high`


---

## Changement dynamique de rôle

**Description :** Le super-médecin peut switcher de rôle pour tester

**Labels :** `super-médecin,auth,type:feature,priority:medium`


---
S7

## Gestion des comptes utilisateurs (CRUD)

**Description :** Créer, modifier, désactiver un utilisateur

**Labels :** `admin,backend,type:feature,priority:high`


---

## Logs d’activité

**Description :** Consulter les logs techniques des utilisateurs

**Labels :** `admin,sécurité,type:feature,priority:medium`


---

## Super Admin : changer de rôle à la volée

**Description :** Option visible uniquement par super admin

**Labels :** `super-admin,auth,type:feature,priority:medium`


---
