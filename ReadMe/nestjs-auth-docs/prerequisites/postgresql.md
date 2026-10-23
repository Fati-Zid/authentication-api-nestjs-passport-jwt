# PostgreSQL

## Qu’est-ce que PostgreSQL ?

PostgreSQL est un système de gestion de base de données relationnelle (SGBDR). Il permet de stocker les données dans des tables et de définir des relations entre elles. Il prend également en charge les contraintes d’intégrité et les transactions.

## À quoi sert-il dans notre projet ?

On va utiliser PostgreSQL pour conserver les informations de nos utilisateurs. Notre table `user` pourra contenir un identifiant unique, une adresse email, un mot de passe haché et des dates de création et de modification.

Lorsqu’un utilisateur se connecte, notre application recherchera son compte dans la base de données pour vérifier les identifiants fournis.

## Pourquoi ce choix ?

PostgreSQL permet de structurer les données, d’imposer des contraintes comme l’unicité de l’email et de garantir la cohérence des opérations grâce aux transactions. Ces fonctionnalités sont utiles pour éviter, par exemple, que deux comptes soient créés avec la même adresse email.

## Comment fonctionne-t-il avec TypeORM ?

PostgreSQL conserve les données. TypeORM facilite les interactions entre notre application TypeScript et la base de données.

## À retenir

PostgreSQL stocke les données. La vérification des identifiants est une responsabilité de notre application, et non de la base de données elle-même.

Documentation : [PostgreSQL](https://www.postgresql.org/docs/)
