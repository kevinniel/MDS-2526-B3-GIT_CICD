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
    - `hotfix` : se tire de `main` & se merge sur `develop` & `main` pour corriger des bugs en production.