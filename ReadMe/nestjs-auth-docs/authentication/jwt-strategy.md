# JWT Strategy

## Qu’est-ce que la JWT Strategy ?

La stratégie JWT de Passport permet d’extraire un jeton d’une requête et de vérifier qu’il est valide selon la configuration de l’application.

## Comment fonctionne-t-elle ?

1. Après une connexion réussie, le serveur remet un JWT au client.
2. Le client envoie le jeton dans l’en-tête `Authorization`, généralement sous la forme `Bearer <token>`.
3. La stratégie extrait le jeton et vérifie notamment sa signature et son expiration.
4. Si le jeton est valide, la stratégie peut fournir les informations d’utilisateur à la suite du traitement de la requête.
5. Si le jeton est invalide ou expiré, l’accès à la route protégée est refusé.

## Pourquoi l’utiliser ?

Elle évite de demander à l’utilisateur ses identifiants à chaque requête et permet de centraliser la validation des jetons.

## Points de sécurité

Le serveur doit vérifier la signature et les claims nécessaires, notamment l’expiration. Le contenu d’un JWT signé n’est pas automatiquement chiffré : il ne faut pas y inclure de secrets.

## À retenir

La JWT Strategy valide le jeton envoyé par le client. Un Guard NestJS permet d’appliquer cette stratégie aux routes protégées.

Documentation : [NestJS — Authentication](https://docs.nestjs.com/security/authentication)
