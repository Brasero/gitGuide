# Installation #
Pour utiliser git en ligne de commande, vous devez d'abord l'installer sur votre ordinateur. Si git n'est pas déjà installé sur votre ordinateur, vous pouvez le télécharger à partir du site web de [Git](https://git-scm.com). Suivez les instructions d'installation et assurez-vous que git est ajouté à votre chemin d'accès pour pouvoir l'utiliser depuis n'importe quel dossier.

# Configuration #
Avant de commencer à utiliser git, vous devez configurer votre nom d'utilisateur et votre adresse e-mail. Cela vous permettra de signer vos commits et de savoir qui a apporté des modifications au code. Pour configurer votre nom d'utilisateur et votre adresse e-mail, utilisez les commandes suivantes :

``` 
$ git config --global user.name "John Doe"
$ git config --global user.email "johndoe@example.com"
```
# Créer un nouveau dépôt #

Pour créer un nouveau dépôt git, vous devez d'abord créer un nouveau dossier et y accéder. Une fois dans le dossier, utilisez la commande `git init` pour initialiser le dépôt :

``` 
$ mkdir my-project
$ cd my-project
$ git init
```
Cette commande créera un nouveau sous-dossier appelé `.git` qui contiendra tous les fichiers de configuration et de suivi de version de votre projet.

# Ajouter et committer des fichiers #

Pour ajouter des fichiers à votre dépôt git, utilisez la commande ``git add``. Par exemple, pour ajouter un fichier nommé file.txt, utilisez la commande suivante :

``` 
$ git add file.txt
```
Pour ajouter tous les fichiers modifiés ou nouveaux du répertoire courant, utilisez la commande `git add .`.

Une fois que vous avez ajouté les fichiers que vous souhaitez suivre, vous devez les "committer" avec un message de commit qui décrit les modifications apportées. Utilisez la commande `git commit` pour committer les fichiers :

``` 
$ git commit -m "Ajout du fichier file.txt"
```

# Synchroniser son repo #

Pour synchroniser votre dépôt local avec un dépôt distant, vous devez d'abord ajouter le dépôt distant à votre dépôt local. Pour ce faire, utilisez la commande `git remote add origin <url>` :

```
$ git remote add origin https://github.com/username/my-project.git
```
Cette commande ajoute un nouveau dépôt distant appelé `origin` à votre dépôt local. Vous pouvez ensuite utiliser la commande `git push` pour envoyer vos commits vers le dépôt distant :

```
$ git push -u origin master
```
Cette commande enverra tous les commits de la branche `master` vers le dépôt distant appelé `origin`.

# Récupérer les modifications d'un repo distant #

Pour récupérer les modifications d'un dépôt distant, vous devez d'abord ajouter la branche distante à votre dépôt local avec la commande `git remote add origin <url>` si ça n'est pas déjà fait.

Cette commande ajoute un nouveau dépôt distant appelé `origin` à votre dépôt local. Vous pouvez ensuite utiliser la commande `git pull` pour récupérer les modifications du dépôt distant :

```
$ git pull origin master
```

Cette commande récupérera toutes les modifications de la branche `master` du dépôt distant appelé `origin`.

# Créer une nouvelle branche #

Pour créer une nouvelle branche, utilisez la commande `git branch` :

```
$ git branch new-branch
```

Cette commande créera une nouvelle branche appelée `new-branch`. Vous pouvez ensuite utiliser la commande `git checkout` pour basculer sur cette nouvelle branche :

```
$ git checkout new-branch
```

Cette commande basculera sur la branche `new-branch`.

# Fusionner une branche #

Pour fusionner une branche avec la branche courante, utilisez la commande `git merge` :

```
$ git merge new-branch
```

Cette commande fusionnera la branche `new-branch` avec la branche courante.

# Supprimer une branche #

Pour supprimer une branche, utilisez la commande `git branch -d` :

```
$ git branch -d new-branch
```

Cette commande supprimera la branche `new-branch`.

# Récupérer les modifications d'une branche distante #

Pour récupérer les modifications d'une branche distante, vous devez d'abord ajouter la branche distante à votre dépôt local avec la commande `git remote add origin [url]` si ça n'est pas déjà fait.
Puis utiliser la commande `git fetch` pour récupérer les modifications de la branche distante :

```
$ git fetch
```

Vous pouvez ensuite utiliser la commande `git pull` pour récupérer les modifications de la branche distante :

```
$ git pull
```

Cette commande récupérera toutes les modifications de la branche sur la quel vous êtes du dépôt distant appelé `origin`.
