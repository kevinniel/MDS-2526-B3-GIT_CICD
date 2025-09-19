# Cours de GIT

## Rappel des bases

- Créé par Linus Torvalds en 2005
- Permet de réaliser du versionning (gestion de versions, gestion de l'historique)
- Permet le travail collaboratif (plusieurs personnes sur un même projet, et garantir l'intégrité du travail de chacun)

## Vocabulaire

- `Dossier courant` : C'est le dossier depuis lequel on exécute une commande.
- `Repository` : C'est un dossier qui "utilise" GIT : il dispose d'un sous-dossier caché ".git". Ils peuvent être distants ou locaux.
- `Repository local` : C'est le repository qui est sur une machine à laquelle vous avez généralement accès.
- `Repository distant` : C'est le repository qui est **hébergé et géré** par une plateforme spécialisée (Github, Gitlab, Gitea, etc...). Ils peuvent être publics (accessibles à tous) ou privés (accessibles uniquement à ceux qu'on souhaite).
- `Les branches` : Permettent de gérer plusieurs versions d'un même projet.
- `conflit` : C'est l'événement qui se déclenche lorsque l'intégrité du travail n'est plus assurée.

## Commandes

- `git init` : Permet de créer un repository local dans le dossier courant.
- `git remote add origin <url>` : Permet de relier un repository local à un repository distant
- `git clone <url> <folder>` : Permet de créer un repository local à partir du contenu d'un repository distant. Lie automatiquement les deux repository.
- `git add <param>` : Permet d'indexer les fichiers/dossiers passées dans `<param>`.
- `git rm <param>` : Permet de désindexer les fichiers/dossiers passées dans `<param>`.
- `git commit -m "<message>"` : Permet de sauvegarder un état d'indexation. Permet également de décrire le commit grâce au message qui est **obligatoire**. Ils sont datés.
- `git push` : Permet d'envoyer les commits du repository local sur le repository distant. Lors du premier push sur une branche, il faudra utiliser la commande `git push -u origin <branch>`. Si vous l'oubliez, GIT vous le rapellera.
- `git pull` : Permet de récupérer les commits du repository distant sur le repository local.
- `git status` : Permet de voir l'état de la branche actuelle du repository local.
- `git log` : Permet de voir l'historique des commits.
- `git reset --hard` : Permet de supprimer toutes les modifications non commitées.
- `git branch` : Permet de lister les branches du repository local et de voir quelle est la branche active.
- `git branch <nom>` : Permet de créer une branche nommée sur le repository local.
- `git branch -d <nom>` : Permet de supprimer une branche sur un repository local.
- `git push origin --delete` : Permet de propager à distance le suppression de branches en local.
- `git checkout <nom>` : Permet de rendre la branche `<nom>` active (= changer de branche 🙈).
- `git merge <nom>` : Permet de fusionner la branche `<nom>` avec la branche active.
- `git rebase <branch>` : Permet de mettre à jour la branche courante à partir de la branche `<branch>`

## Gestion des conflits

- TOTO





## PB Exo

1. Gestion de projet : pas d'orga = c'est la 💩
2. Quand la conception est mauvaise !
