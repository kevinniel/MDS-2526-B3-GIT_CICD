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

## Commandes

- `git init` : Permet de créer un repository local dans le dossier courant.
- `git remote add origin <url>` : Permet de relier un repository local à un repository distant
- `git clone <url> <folder>` : Permet de créer un repository local à partir du contenu d'un repository distant. Lie automatiquement les deux repository.
- `git add <param>` : Permet d'indexer les fichiers/dossiers passées dans `<param>`.
- `git remove <param>` : Permet de désindexer les fichiers/dossiers passées dans `<param>`.
- `git commit -m "<message>"` : Permet de sauvegarder un état d'indexation. Permet également de décrire le commit grâce au message qui est **obligatoire**. Ils sont datés.
- `git push` : Permet d'envoyer les commits du repository local sur le repository distant. En cas de changement de branche ou lors du premier push, il faudra utiliser la commande `git push -u origin <branch>`. Si vous l'oubliez, GIT vous le rapellera.
- `git pull` : Permet de récupérer les commits du repository distant sur le repository local.
- `git status` : Permet de voir l'état de la branche actuelle du repository local.
- `git log` : Permet de voir l'historique des commits.




rebase
reset
merge
branch
switch (checkout ???)


