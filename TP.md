# Projet – Gérer un projet complet avec Git Flow et GitHub

Travail en groupes de 3 étudiants, 1 groupe de 4 uniquement. Vous avez jusqu'à demain 10h30 pour terminer.

## 1 – Recherche et compréhension

Chaque groupe crée un document RECHERCHE.md contenant :

1. Une présentation de Git Flow :
    - Historique, objectifs, principes.
    - Description des branches principales et secondaires.
    - Avantages / limites.
2. Une explication du versionnement sémantique (SemVer) :
    - Signification des numéros de version (MAJOR.MINOR.PATCH).
    - Exemples concrets.
3. Le rôle du changelog et de la documentation de version.
4. Le lien entre issues, milestones, et releases sur GitHub (avec schéma ou capture).

## 2 – Mise en place du projet

Créer un dépôt GitHub propre et préparer le workflow Git Flow.

1. Créez un dépôt nommé : `projet-gitflow-groupeX`
2. Initialisez les branches :
    - `main` → production  
    - `develop` → développement
3. Créez un fichier **`README.md`** :
    - Présentation du projet fictif (ex. “Application de gestion d’événements”)  
    - Schéma du workflow Git Flow  
    - Légende des branches
4. Créez une **milestone** : `v1.0 - Première version stable`
5. Ajoutez des **issues** :
    - Création du README  
    - Organisation de la structure du dépôt  
    - Ajout d’un changelog  
    - Simulation d’une première fonctionnalité  
    - Simulation d’un correctif (hotfix)
6. Créez un **Project (Kanban)** pour suivre les issues.

## 3 - Simulation complète du cycle Git Flow

### Étape 1 – Développement (features)

Chaque membre :
1. Crée une branche `feature/nom-feature` (ex : `feature/readme`, `feature/logo`, `feature-doc`)
2. Ajoute du contenu symbolique (fichiers texte, docs/, maquettes, etc.)
3. Ouvre une **Pull Request** vers `develop`
4. Demande une **review**
5. Merge une fois approuvée
6. Lie la PR à une issue : `Fixes #3`

### Étape 2 – Préparation de la release

1. Créez une branche `release/1.0.0` depuis `develop`
2. Créez un fichier **`CHANGELOG.md`** :
```markdown
    # Changelog
    ## [1.0.0] - 2025-10-07
    ### Ajouté
    - Structure du projet
    - README et documentation Git Flow
    - Processus de contribution (CONTRIBUTING.md)
```
3. Merge release/1.0.0 → main
4. Créez un tag GitHub : v1.0.0
5. Fermez la milestone correspondante

### Étape 3 – Correctif (hotfix)

1. Créez hotfix/1.0.1 depuis main
2. Modifiez un fichier mineur (typo, info manquante)
3. Créez une PR vers main
4. Merge et taguez v1.0.1

### Étape 4 - Documentation & présentation finale

1. Finalisez :
    - README.md (structure, workflow, version actuelle)
    - CHANGELOG.md (versions 1.0.0 et 1.0.1)
    - RECHERCHE.md
    - Nouveau fichier RETEX.md :
        - Ce que vous avez appris sur Git et GitHub
        - Les difficultés rencontrées et comment vous les avez résolues
        - Les erreurs ou bonnes pratiques que vous retiendrez pour vos futurs projets
2. Nettoyez le dépôt :
    - Supprimez les branches inutiles
    - Fermez les issues terminées
    - Vérifiez que la milestone est bien clôturée
3. Vérifiez que tout est cohérent :
    - Le changelog correspond aux versions taguées
    - Les PR sont liées aux issues
    - Le board GitHub reflète l’état final du projet

## Intégration CI/CD

Vous allez maintenant automatiser plusieurs vérifications et actions sur votre dépôt via GitHub Actions. Chaque script doit être placé dans le dossier : `.github/workflows/` et enregistré avec une extension .yml.

### Étape 1 – Fermeture automatique des issues

Créez un workflow CI/CD qui :

- Se déclenche à chaque push sur toutes les branches.
- Analyse les messages de commits.
- Ferme automatiquement les issues mentionnées avec des mots-clés comme : `Fixes #1, Closes #2, Resolves #3`.
- Ajoute un commentaire automatique sur l’issue indiquant la branche et le commit qui ont provoqué la fermeture.
- Ignore les Pull Requests (ne doit fermer que des issues).

### Étape 2 – Vérification du changelog

Mettez en place un workflow CI qui automatise la vérification du fichier CHANGELOG.md.


## Groupes 

1 : nathan + ad + Matthis r.
2 : Quentin + Bridou + Robin
3 : Léo + Alexandre + Camille
4 : Mattis b. + Mathis h + Frédéric + damien



test