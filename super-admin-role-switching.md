# Guide d'utilisation : Changement de rôle pour Super Admin

## Introduction

La fonctionnalité "Changer de rôle à la volée" permet aux utilisateurs Super Admin de naviguer temporairement dans l'application avec les droits d'un autre rôle. Ceci est particulièrement utile pour tester et vérifier l'expérience utilisateur des différents profils d'utilisateurs sans avoir besoin de se déconnecter et de se reconnecter avec un autre compte.

## Prérequis

- Vous devez avoir le rôle **Super Admin** pour accéder à cette fonctionnalité
- Être connecté à l'application OneClickMedical

## Comment changer temporairement de rôle

### 1. Accéder à la fonctionnalité

La fonctionnalité est accessible de deux façons :

- **Dans le menu latéral** : Un indicateur discret apparaît sous votre nom et votre rôle actuel si vous êtes Super Admin.

![Indicateur de changement de rôle](../assets/images/role-switch-indicator.png)

### 2. Sélectionner un nouveau rôle

1. Cliquez sur le bouton "Changer de rôle"
2. Une fenêtre modale s'affiche avec les différents rôles disponibles :
   - Patient
   - Infirmier
   - Médecin
   - Super Médecin
   - Admin
3. Sélectionnez le rôle souhaité en cliquant sur son option
4. Cliquez sur le bouton "Changer de rôle" en bas à droite de la fenêtre

![Modal de changement de rôle](../assets/images/role-switch-modal.png)

> **Note :** Vous pouvez fermer cette fenêtre à tout moment en cliquant en dehors de la fenêtre modale, ou sur le bouton "Annuler".

### 3. Navigation avec le rôle temporaire

Une fois que vous avez changé de rôle :

- L'interface se rafraîchit automatiquement
- Vous verrez une indication claire que vous utilisez un rôle temporaire
- Vous n'aurez accès qu'aux fonctionnalités disponibles pour ce rôle
- Le menu de navigation s'adaptera aux permissions du nouveau rôle

![Indicateur de rôle temporaire](../assets/images/temporary-role-indicator.png)

## Comment revenir à votre rôle Super Admin

### 1. Accéder à la fonctionnalité de retour

Lorsque vous utilisez un rôle temporaire, l'indicateur dans la barre latérale change pour afficher :
- "Rôle temporaire : [Nom du rôle]"

### 2. Revenir au rôle Super Admin

1. Cliquez sur l'indicateur de rôle temporaire
2. Une fenêtre modale s'affiche avec l'option de revenir à votre rôle d'origine
3. Cliquez sur le bouton "Revenir au rôle Super Admin"

![Modal de retour au rôle Super Admin](../assets/images/revert-role-modal.png)

> **Note :** Vous pouvez également fermer cette fenêtre en cliquant en dehors de la modale.

### 3. Confirmation du retour

- L'interface se rafraîchit automatiquement
- Vous récupérez toutes les permissions de Super Admin
- L'indicateur de rôle temporaire disparaît

## Aspects importants à noter

1. **Sécurité** : Cette fonctionnalité est uniquement disponible pour les utilisateurs ayant le rôle Super Admin
2. **Temporaire** : Le changement de rôle est temporaire et n'affecte que votre session actuelle
3. **Déconnexion** : Si vous vous déconnectez pendant l'utilisation d'un rôle temporaire, vous serez reconneté avec votre rôle d'origine lors de la prochaine connexion
4. **Compatibilité** : Cette fonctionnalité fonctionne avec tous les rôles disponibles dans le système

## Cas d'utilisation recommandés

- Vérifier l'expérience utilisateur des différents rôles
- Tester les limitations d'accès pour chaque type d'utilisateur
- Former de nouveaux utilisateurs en leur montrant l'interface qu'ils verront
- Diagnostiquer des problèmes d'interface ou de permission signalés par les utilisateurs

## Dépannage

| Problème | Solution |
|---------|----------|
| Le bouton "Changer de rôle" n'apparaît pas | Vérifiez que vous êtes bien connecté avec un compte Super Admin |
| Impossible de revenir au rôle Super Admin | Essayez de rafraîchir la page, puis cliquez à nouveau sur l'indicateur de rôle |
| Interface non mise à jour après changement | Cliquez sur le bouton d'actualisation de votre navigateur |

---

Pour toute assistance supplémentaire concernant cette fonctionnalité, veuillez contacter l'équipe de support technique.

*Dernière mise à jour : 13 juin 2025*
