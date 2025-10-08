# Gitflow

C'est une convention d'utilisation de GIT, permettant une organisation du versionning au sein d'un projet.

## Convention de nommage des versions

__Note__ : c'est à vous de juger de la qualification des changements !

- Major : concerne des changements significatifs dans le projet. Comme par exemple : 
    - changements incompatible avec les versions précédentes ;
    - changement de structure ;
    - changement sur la manière de concevoir le produit ;
    - etc...
- Minor : concerne des changements qui restent compatible avec la version majeure actuelle du projet.
    - ajout de fonctionnalités ;
    - changement d'éléments sans conséquences importantes
- Patch : concerne des correctifs
    - bugs ;
    - fautes d'orthographe ;
    - etc...

La construction du nom se fait de la sorte : `Major.Minor.Patch`.

## C'est un système qui exploite les branches

Chaque branche à un rôle bien définie :
2 branches principales :
    - `main` : branche de production
    - `develop` : branche de développement
Système de branches temporaires et secondaires : 
    - `feature` : se tire de `develop` pour une nouvelle fonctionnalité
    - `release` : se tire de `develop` & se merge sur `develop` & `main` pour implémenter une nouvelle version.
    - `hotfix` : se tire de `main` & se merge sur `develop` & `main` pour corriger des bugs **critiques** en production.

## Le Workflow 

On part du principe que l'on vient de créer un repository tout neuf. Les étapes à mettre place sont : 

1. Créer une branche de développement : `develop`
2. Mettre en place les 4 fichiers de documentation au sein du projet : 
    - README.md
    - CHANGELOG.md
    - LICENSE
    - CONTRIBUTING.md

### Pour la réalisation d'une feature 

1. La mettre en place
    -  Faire une branche `feature/NOM_FEATURE` pour la fonctionnalité à développer
    -  Merger la branche `feature/NOM_FEATURE` sur la branch `develop`
2. Créer une branche `release/vX.Y.Z` à partir de la branche `develop`
    - On teste et on corrige les éventuels bugs 
    - On met à jour le changelog
3. On merge la branche `release/vX.Y.Z` sur la branche `main` & `develop`
4. On crée un tag avec le numéro de version sur le commit du merge vers `main`

### Pour la réalisation d'un hotfix

1. On corrige un bug sur la branche `main`: 
    - Faire une branche `hotfix/vX.Y.Z` pour la fonctionnalité à développer
    - Merger la branche `hotfix/vX.Y.Z` sur la branch `main` & `develop`
2. On crée un tag avec le numéro de version sur le commit du merge vers `main`
