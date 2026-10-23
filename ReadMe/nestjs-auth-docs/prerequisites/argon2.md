# Argon2

## Qu’est-ce qu’Argon2 ?

Argon2 est un algorithme de hachage conçu pour protéger les mots de passe. Il a été sélectionné comme vainqueur de la Password Hashing Competition en 2015.

Contrairement au chiffrement, le hachage est conçu pour être irréversible en pratique : on ne récupère pas le mot de passe original à partir du hachage.

## À quoi sert-il dans notre projet ?

Lorsqu’un utilisateur crée un compte, notre application hache son mot de passe avant de l’enregistrer dans PostgreSQL. Lorsqu’il se connecte, on utilise la fonction de vérification d’Argon2 pour vérifier le mot de passe fourni par rapport au hachage enregistré.

On ne stocke donc jamais le mot de passe en clair.

## Pourquoi ce choix ?

Argon2 est spécialement conçu pour le hachage des mots de passe. Son coût en temps et en mémoire peut être ajusté afin de rendre les attaques par essais répétés plus coûteuses.

## Comment fonctionne-t-il avec les autres outils ?

Notre service utilisateur utilise Argon2 pour hacher et vérifier les mots de passe. TypeORM enregistre le hachage dans PostgreSQL. Passport peut ensuite s’appuyer sur le résultat de cette vérification pour déterminer si l’authentification locale réussit.

## À retenir

Argon2 protège les mots de passe enregistrés. JWT sert à transmettre une preuve d’authentification dans les requêtes suivantes : ce sont deux mécanismes différents.

Documentation : [Argon2 — RFC 9106](https://www.rfc-editor.org/rfc/rfc9106)
