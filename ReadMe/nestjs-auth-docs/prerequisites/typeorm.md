# TypeORM

## Qu’est-ce que TypeORM ?

TypeORM est un ORM (*Object-Relational Mapper*). Il permet de manipuler les données d’une base relationnelle à travers des objets et des entités TypeScript.

Une entité représente la structure d’une table. Un repository permet d’effectuer des opérations sur les données associées à cette entité.

## À quoi sert-il dans notre projet ?

On va définir une entité `User` pour représenter les utilisateurs. On pourra ensuite utiliser un repository pour :

- rechercher un utilisateur par son email ;
- créer un nouvel utilisateur ;
- enregistrer ses informations ;
- vérifier si un compte existe déjà.

## Pourquoi ce choix ?

TypeORM s’intègre à NestJS et prend en charge TypeScript, les entités, les repositories et l’injection de dépendances. Cela nous permet de séparer la logique métier de la logique d’accès aux données.

## Comment fonctionne-t-il avec PostgreSQL ?

Notre application utilise TypeORM pour demander des opérations sur les données. TypeORM traduit ces opérations en requêtes adaptées à PostgreSQL, qui stocke ensuite les résultats.

## À retenir

TypeORM ne remplace pas PostgreSQL. Il facilite l’accès à la base de données depuis notre code TypeScript.

Documentation : [TypeORM](https://typeorm.io/)
