# Documentation — NestJS Authentication

## Introduction

Bienvenue dans la documentation de notre système d’authentification avec NestJS.

L’objectif de ce projet est de comprendre comment construire un système d’authentification sécurisé, modulaire et facile à faire évoluer.

On va avancer étape par étape, en commençant par les outils utilisés, puis en explorant les concepts nécessaires à l’implémentation.

## Documentation

### 1. Prérequis techniques

Avant de commencer à coder, on va comprendre le rôle des outils utilisés dans notre projet.

- [Node.js et npm](prerequisites/nodejs-npm.md)
- [Passport](prerequisites/passport.md)
- [JWT](prerequisites/jwt.md)
- [PostgreSQL](prerequisites/postgresql.md)
- [TypeORM](prerequisites/typeorm.md)
- [Argon2](prerequisites/argon2.md)

### 2. Concepts d’authentification

Dans cette partie, on va découvrir comment fonctionne l’authentification dans NestJS et comment protéger les routes de notre application.

- [Authentification et autorisation](authentication/authentication-vs-authorization.md)
- [Local Strategy](authentication/local-strategy.md)
- [JWT Strategy](authentication/jwt-strategy.md)
- [Guards et décorateurs](authentication/guards-and-decorators.md)

## Notre approche

Pour chaque concept, on va répondre aux questions suivantes :

1. Qu’est-ce que c’est ?
2. À quoi ça sert ?
3. Comment ça fonctionne ?
4. Pourquoi l’utilise-t-on dans notre projet ?
5. Comment s’intègre-t-il avec les autres composants ?
6. Quels sont les points importants à retenir ?

L’objectif est de comprendre les choix techniques avant de passer à l’implémentation.
