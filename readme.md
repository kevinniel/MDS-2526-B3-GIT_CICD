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
- `Fork` : C'est un repository distant propriétaire qui est une copie d'un autre repository distant non propriétaire.
- `Pull Request` : Propose de fusionner un fork vers le repository original.
- `Issue` : "Ticket" géré via le système de ticketing de github.

## Commandes

- `git init` : Permet de créer un repository local dans le dossier courant.
- `git remote add origin <url>` : Permet de relier un repository local à un repository distant
- `git clone <url> <folder>` : Permet de créer un repository local à partir du contenu d'un repository distant. Lie automatiquement les deux repository.
- `git add <param>` : Permet d'indexer les fichiers/dossiers passées dans `<param>`.
- `git rm <param>` : Permet de désindexer les fichiers/dossiers passées dans `<param>`.
- `git commit -m "<message>"` : Permet de sauvegarder un état d'indexation. Permet également de décrire le commit grâce au message qui est **obligatoire**. Ils sont datés.
- `git commit -m "Fixes #20"` : Permet de clore automatiquement l'issue #20, en la liant au commit.
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

## Les conflits

### Comment les gérer ?

Ils peuvent concerner 1 ou plusieurs fichiers

Lorsqu'ils apparaissent, plusieurs options sont possibles :
1. Garder l'ancienne version du fichier et supprimer la nouvelle.
2. Garder la nouvelle version du fichier et supprimer l'ancienne.
3. Garder les deux versions.

Pour identifier un conflit dans un fichier, 3 parties :
- Le début est symbolisé par une série de caractères `<<<<<<<<<<<`
- La fin est symbolisé par une série de caractères `>>>>>>>>> <id_commit>`
- Pour délimiter le code "avant" du code "après", GIT insère une série de caractères `=======`

### Astuces pour les éviter ?

1. L'organisation permet largement d'éviter les conflits ou à minima de les limiter.
2. Penser à `git pull` avant de `git push` permet d'éviter d'en avoir.
3. C'est normal d'en rencontrer, même avec les meilleures pratiques.

## Votre profil Github

Github vous permet de créer un "profil" et de le présenter proprement. Pour en mettre en place :

1. créer un repository qui ait **EXACTEMENT** le même nom que votre pseudo.
2. créer un fichier readme.md dedans et le remplir
3. consultez l'url : https://github.com/VOTRE_PSEUDO

Le contenu du fichier readme devrait s'afficher !

## Les bonnes pratiques

- Les commentaires de vos commits doivent être explicites. Si vous avez oublier de nommer correctement le dernier, faites un `git commit --amend`.
- intégrer les gitmoji : https://gitmoji.dev/
- Avoir un beau profil (ex : https://github.com/abhisheknaiidu/awesome-github-profile-readme?tab=readme-ov-file)




Je vais créer des Issues, je veux que les concernés s'en occupent. Une fois qu'ils ont terminé, ils doivent modifier le contenu de leur fichier texte pour dire ce qu'ils ont fait.