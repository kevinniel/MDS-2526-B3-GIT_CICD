# CI/CD

## Signification

CI/CD : Continuous Integration / Continuous Deployment

L'intégration continue est le fait de contrôler la qualité et l'intégrité du code de manière automatique (par exemple avec des tests, des linters etc...).
Le déploiement continue réside dans le fait de dépoyer automatiquement vos modifications si - et seulement si - le contrôle de la qualité à été validé.

## Comment ça fonctionne ?

On défini des pipelines : c'est un workflow d'actions que l'on a paramétré pour se déclencher dans des conditions très spécifiques.

On doit activer ces pipelines pour les rendre fonctionnels.

## Sur Github

On utilise un système qui s'appelle `Github Actions`.
Dans Github Actions, un pipeline est représenter par un fichier au format YAML (.yml).
Chaque pipeline doit être positionné dans le dossier `.github/workflows`.
Lors de chaque déclencheur, l'ensemble des pipelines font s'exécuter.

**Liens utiles** : 

- Liste des déclencheurs (à droite) : https://docs.github.com/fr/actions/reference/workflows-and-actions/events-that-trigger-workflows
- Marketplace : https://github.com/marketplace?type=actions
