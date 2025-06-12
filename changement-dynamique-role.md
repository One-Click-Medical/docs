# Guide d'utilisation : Changement dynamique de rôle

## Vue d'ensemble

La fonctionnalité de **changement dynamique de rôle** permet aux utilisateurs disposant de privilèges élevés (Super-médecin et Super-admin) de changer temporairement leur rôle dans l'application pour accéder aux fonctionnalités spécifiques à d'autres rôles. Cette fonctionnalité est particulièrement utile pour tester l'application du point de vue des différents utilisateurs, vérifier les droits d'accès, et former de nouveaux utilisateurs en leur montrant les interfaces des différents rôles.

## Accès à la fonctionnalité

1. La fonctionnalité n'est disponible que pour les utilisateurs ayant les rôles suivants :
   - **Super-médecin** : Peut tester les rôles Médecin et Infirmier
   - **Super-admin** : Peut tester les rôles Admin, Médecin, Infirmier et Patient

2. Pour accéder à cette fonctionnalité :
   - Connectez-vous avec un compte disposant des droits appropriés
   - Naviguez vers la page **"Mon Profil"** accessible depuis le menu latéral ou l'icône de profil dans l'en-tête
   - La section "Changement de rôle temporaire" apparaît en haut de la page

## Utilisation du changement de rôle

### Changer de rôle temporairement

1. Dans la section **"Changement de rôle temporaire"**, vous trouverez une liste déroulante contenant les rôles disponibles pour vous
2. Sélectionnez le rôle que vous souhaitez tester dans la liste déroulante
3. Cliquez sur le bouton **"Changer de rôle"**
4. Une notification de confirmation apparaît et l'interface se met à jour automatiquement

![Interface de changement de rôle](../assets/images/role_switcher_interface.png)

### Indicateurs de mode test

Lorsque vous utilisez un rôle temporaire, plusieurs indicateurs visuels vous le rappellent :

1. Dans la page de profil, une **alerte orange** apparaît indiquant :
   - Le rôle temporaire actuellement utilisé
   - Votre rôle d'origine
   
2. Un bouton **"Revenir à mon rôle d'origine"** remplace la liste déroulante

![Mode test activé](../assets/images/role_switcher_active.png)

### Revenir à votre rôle d'origine

Pour revenir à votre rôle d'origine :

1. Allez sur la page **"Mon Profil"**
2. Dans la section "Changement de rôle temporaire", cliquez sur le bouton **"Revenir à mon rôle d'origine"**
3. Une notification de confirmation apparaît et l'interface se met à jour automatiquement

## Limitations et remarques importantes

1. **Durée de session** : Le changement de rôle est valable jusqu'à ce que vous :
   - Reveniez manuellement à votre rôle d'origine
   - Vous déconnectiez de l'application

2. **Sécurité** : 
   - Les actions effectuées en mode test sont journalisées avec votre identité originale dans les logs système
   - Certaines actions administratives sensibles peuvent rester inaccessibles même en mode test

3. **Interface utilisateur** :
   - Toutes les fonctionnalités disponibles pour le rôle sélectionné deviennent accessibles
   - Le menu de navigation s'adapte automatiquement pour afficher uniquement les pages disponibles pour ce rôle

## Cas d'utilisation courants

### Pour les Super-médecins

- **Test des fonctionnalités médecin** : Vérifiez l'expérience des médecins standards pour la prise de rendez-vous et la consultation des dossiers patients
- **Test des fonctionnalités infirmier** : Validez le flux de travail des soins infirmiers et l'accès aux observations

### Pour les Super-admins

- **Test du tableau de bord administrateur** : Explorez les fonctionnalités d'administration avec des droits limités
- **Test de l'expérience patient** : Vérifiez la prise de rendez-vous et la consultation des dossiers du point de vue du patient
- **Formation et support** : Démonstration des différentes interfaces pour former les nouveaux utilisateurs

## Dépannage

| Problème | Solution possible |
|---------|------------------|
| Le bouton "Changer de rôle" ne fait rien | Vérifiez votre connexion internet et rafraîchissez la page |
| Impossible de revenir au rôle d'origine | Déconnectez-vous et reconnectez-vous à l'application |
| Certaines fonctionnalités restent inaccessibles | Certaines actions peuvent être restreintes même en mode test pour des raisons de sécurité |

---

Pour toute assistance supplémentaire concernant cette fonctionnalité, veuillez contacter l'équipe de support OneClickMedical.
