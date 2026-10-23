# Authentification et autorisation

## Qu’est-ce que l’authentification ?

L’authentification consiste à vérifier l’identité d’un utilisateur. Dans notre application, cela peut se faire en vérifiant son adresse email et son mot de passe.

## Qu’est-ce que l’autorisation ?

L’autorisation détermine les ressources auxquelles un utilisateur authentifié peut accéder et les actions qu’il peut effectuer.

## Quelle est la différence ?

- **Authentification** : vérifier qui est l’utilisateur.
- **Autorisation** : déterminer ce que cet utilisateur a le droit de faire.

Par exemple, se connecter à une application permet de vérifier l’identité d’un utilisateur. En revanche, accéder à une page réservée aux administrateurs dépend de ses permissions.

## Pourquoi cette distinction est-elle importante ?

Un utilisateur authentifié ne doit pas automatiquement avoir accès à toutes les ressources. Notre application doit vérifier les permissions requises pour les opérations sensibles.

## À retenir

Être authentifié ne signifie pas avoir accès à toutes les ressources de l’application.
