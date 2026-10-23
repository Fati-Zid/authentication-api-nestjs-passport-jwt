# Guards et décorateurs dans NestJS

## Qu’est-ce qu’un Guard ?

Un Guard est une classe NestJS qui implémente l’interface `CanActivate`. Il détermine si une requête peut continuer vers une route ou un gestionnaire de contrôleur.

## À quoi sert-il dans notre système ?

On va utiliser un Guard d’authentification pour appliquer la stratégie JWT aux routes protégées. Avant d’exécuter la route, le Guard vérifie que la requête satisfait aux conditions d’authentification.

## Qu’est-ce qu’un décorateur ?

Un décorateur est une fonction qui permet d’ajouter des métadonnées ou un comportement à une classe, une méthode ou une propriété, selon le type de décorateur.

Dans notre projet, on peut créer un décorateur personnalisé comme `@Public()` pour marquer les routes qui ne nécessitent pas d’authentification.

## Comment le Guard et le décorateur fonctionnent-ils ensemble ?

1. Le décorateur `@Public()` ajoute une métadonnée à la route.
2. Le Guard utilise `Reflector` pour lire cette métadonnée.
3. Si la route est publique, le Guard laisse passer la requête sans appliquer la validation JWT.
4. Sinon, il applique la stratégie d’authentification.

## Pourquoi cette approche ?

Elle permet de protéger les routes par défaut tout en déclarant clairement les exceptions publiques. Il faut configurer le Guard globalement et s’assurer que la vérification des métadonnées est correcte.

## À retenir

Le Guard prend la décision d’autoriser ou non la poursuite de la requête. Le décorateur `@Public()` fournit une métadonnée que le Guard peut consulter.

Documentation : [NestJS — Guards](https://docs.nestjs.com/guards) · [NestJS — Custom decorators](https://docs.nestjs.com/custom-decorators)
