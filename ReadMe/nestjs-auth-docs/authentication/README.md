# Concepts d’authentification

Dans cette partie, on va découvrir les concepts nécessaires pour comprendre le système d’authentification de notre application NestJS.

- [Authentification et autorisation](authentication-vs-authorization.md)
- [Local Strategy](local-strategy.md)
- [JWT Strategy](jwt-strategy.md)
- [Guards et décorateurs](guards-and-decorators.md)

## Comment les composants collaborent-ils ?

1. L’utilisateur envoie ses identifiants.
2. Notre application recherche son compte à l’aide de TypeORM et PostgreSQL.
3. Argon2 vérifie le mot de passe fourni par rapport au hachage enregistré.
4. La stratégie Local de Passport valide les identifiants.
5. Si l’authentification réussit, l’application génère un JWT signé.
6. Le client envoie le jeton avec ses requêtes suivantes.
7. Un Guard NestJS applique la stratégie JWT pour valider le jeton avant de permettre l’accès à une route protégée.

Être authentifié ne signifie pas automatiquement avoir le droit d’effectuer toutes les actions. La vérification des permissions relève de l’autorisation.
