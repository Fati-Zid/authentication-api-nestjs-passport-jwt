# Local Strategy

## Qu’est-ce que la Local Strategy ?

La stratégie Local de Passport permet d’authentifier un utilisateur à partir d’identifiants fournis directement, généralement un nom d’utilisateur ou un email et un mot de passe.

## Comment fonctionne-t-elle ?

1. Le client envoie ses identifiants à une route de connexion.
2. La stratégie Local transmet les valeurs à la logique de validation.
3. Notre application recherche le compte dans PostgreSQL via TypeORM.
4. Argon2 vérifie le mot de passe fourni par rapport au hachage enregistré.
5. Si les identifiants sont valides, l’authentification réussit ; sinon, la connexion est refusée.

## Pourquoi l’utiliser ?

Elle permet de séparer la vérification des identifiants du reste du contrôleur et de s’appuyer sur le système de stratégies de Passport.

## Comment s’intègre-t-elle à NestJS ?

On peut utiliser `@nestjs/passport` et `passport-local`, puis appliquer un Guard basé sur la stratégie Local à la route de connexion.

## À retenir

La Local Strategy vérifie les identifiants de connexion. Elle ne génère pas à elle seule le JWT ; la génération du jeton est généralement gérée ensuite par notre service d’authentification.

Documentation : [NestJS — Authentication](https://docs.nestjs.com/security/authentication)
