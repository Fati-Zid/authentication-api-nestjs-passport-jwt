# JWT (JSON Web Token)

## Qu’est-ce que JWT ?

JWT signifie *JSON Web Token*. Il s’agit d’un format standard permettant de transmettre des informations sous forme de jeton signé.

Un JWT contient généralement trois parties : un en-tête, un contenu appelé *payload* et une signature. Le payload peut contenir des informations appelées *claims*, par exemple l’identifiant de l’utilisateur et la date d’expiration du jeton.

## À quoi sert-il dans notre projet ?

Une fois les identifiants vérifiés, on va générer un JWT. Le client pourra ensuite envoyer ce jeton avec ses prochaines requêtes. Notre application vérifiera notamment sa signature et son expiration avant de l’accepter comme preuve d’authentification.

## Pourquoi ce choix ?

JWT permet de transmettre des informations d’authentification dans un format standard. Il est utile lorsqu’on veut authentifier plusieurs requêtes sans demander à l’utilisateur de saisir ses identifiants à chaque fois.

## Comment fonctionne-t-il avec Passport ?

Passport peut utiliser une stratégie JWT pour extraire le jeton d’une requête et le valider. Dans NestJS, un Guard peut ensuite appliquer cette stratégie aux routes protégées.

## Points de sécurité

Un JWT signé n’est pas nécessairement chiffré. Son contenu peut généralement être lu par celui qui possède le jeton. On ne doit donc jamais y placer un mot de passe ou d’autres secrets. Il faut également définir une expiration et protéger le jeton côté client.

## À retenir

JWT est le format du jeton. Passport fournit la stratégie qui permet de le vérifier.

Documentation : [Introduction à JWT](https://www.jwt.io/introduction#when-to-use-json-web-tokens) · [NestJS — Authentication](https://docs.nestjs.com/security/authentication)
