# Passport

## Qu’est-ce que Passport ?

Passport est un middleware d’authentification pour Node.js. Il permet d’intégrer différentes stratégies d’authentification selon les besoins de l’application.

Une stratégie définit comment l’application vérifie l’identité d’un utilisateur.

## À quoi sert-il dans notre projet ?

On va utiliser notamment deux stratégies :

- **Local Strategy** : vérifier les identifiants, comme l’email et le mot de passe.
- **JWT Strategy** : vérifier le jeton JWT envoyé lors d’une requête.

Dans NestJS, on peut intégrer ces stratégies à l’aide de `@nestjs/passport` et utiliser des Guards pour protéger les routes.

## Pourquoi ce choix ?

On choisit Passport parce qu’il propose une architecture fondée sur les stratégies. Cela permet de séparer les mécanismes d’authentification et de les faire évoluer plus facilement.

## Comment fonctionne-t-il avec les autres outils ?

La stratégie Local peut vérifier les identifiants en faisant appel à notre logique métier. La stratégie JWT valide le jeton envoyé par le client. Les Guards NestJS permettent d’appliquer ces stratégies aux routes.

## À retenir

Passport organise les stratégies d’authentification. Il ne remplace ni la base de données ni le mécanisme de hachage des mots de passe.

Documentation : [Passport.js](https://www.passportjs.org/) · [NestJS — Authentication](https://docs.nestjs.com/security/authentication)
