## Git & Github

#### Sommaire

1. [Qu'est-ce que GIT ?](#what-is-git)
2. [Pourquoi apprendre GIT ?](#why-git)
3. [Installer GIT et créer son compte Github](#install)
4. [Initialiser GIT](#init)
5. [git add & git status](#add-status)
6. [git rm](#rm)
7. [git checkout--](#checkout)
8. [git commit](#commit)
9. [.gitignore](#gitignore)
10. [Les Branches](#branche)
11. [Github Repository](#repo)
12. [README](#readme)
13. [git clone](#clone)

### 1 - Qu'est-ce que GIT ? <a name='what-is-git'></a>

- C'est un controleur de version (Version Control system VCS)
- Il nous permet de gérer nos différents projets et les héberger sur une plateforme tel que Github
- Il nous permet aussi de tracker tous les changements apportés sur le projet

Git est l'outil qui permet de gérer nos différents projets et github est la plateforme qui va héberger ces projets GIT

### 2 - Pourquoi apprendre GIT ? <a name='why-git'></a>

- Pour la collaboration, on peut facilement voir les changements apportés au code par les différents codeurs
- Avoir un historique des versions de votre code pour pouvoir revenir en arrière notamment
- Développer en parallè avec le system de branch

### 3 - Installer GIT et créer son compte Github <a name='install'></a>

- Il faut d'abord installer [GIT bash](https://git-scm.com/downloads) (faites l'installation par défaut)
- Créez votre compte sur [Github](https://github.com)

### 4 - Initialiser GIT <a name='init'></a>

- Créez votre projet puis placez vous dedans avec votre terminal préféré
- Tapez la commande `git init`, ceci va générer un fichier caché .git qui va initialiser GIT dans votre projet
- Si ce n'est pas déjà le cas, enregistrez vos informations d'utilisateur via votre terminal avec cette commande `git config --global user.name 'votreNom'`
- Répétez l'opération pour y enregistrer votre mail `git config --global user.email 'votreemail@exemple.com'`

### 5 - git add & git status <a name='add-status'></a>

- Ensuite il faut ajouter les fichiers/dossiers de notre projet avec la commande `git add nomdufchier` ou `git add .` pour tout ajouter
- Imagineons que nous voulions ajouter tous les fichiers html et css, on peut faire la commande suivante `git add *.html *.css`
- La commande `git status` permet de nous donner le status de nos fichiers dans le projet (en vert ils sont add, en rouge ils ne sont pas add)

### 6 - git rm <a name='rm'></a>

- On peut enlever un fichier qui a été add avec la commande `git rm --cached nomdufichier` ou un dossier avec tous ses fichiers avec `git rm -r --cached nomdudossier` ou encore `git rm -r --cached .` pour enlever tous les fichiers add (attention, si on ne met pas les tirets on supprime le fichier)

### 7 - git checkout-- <a name='checkout'></a>

- On peut supprimer des changements fait précédemment avec la commande `git checkout-- .` (on a pris tout le dossier et on est revenu en arrière)

### 8 - git commit <a name='commit'></a>

- On utilise la commande `git commit -m 'première sauvegarde'` pour sauvegarder nos fichiers, on doit toujours ajouter un commentaire qui représente notre changement

### 9 - .gitignore <a name='gitignore'></a>

- On peut créer un fichier .gitignore, tous les fichiers que nous renseignerons dedans seront ignorés par GIT et ne seront donc pas commit

### 10 - Les Branches <a name='branche'></a>

- On peut créer une autre branche avec la commande `git branch nomdelabranche`
- On peut ensuite se déplacer dans cette branche avec la commande `git checkout nomdelabranche`
- La commande `git branch --list` nous permet de voir la liste des branches
- Une fois dans cette nouvelle branche nous pouvons effectuer des changements, les add et les commit dans cette branche
- Lorsque l'on re bascule sur une autre branche, les changements qui ont été commit auront disparus
- On peut fusionner nos 2 branches en une seule avec la commande `git merge nomdelabranche` depuis l'autre branche

### 11 - Github Repository <a name='repo'></a>

- Créez un nouveau "dépôt" en créant un "New repository"
- Nommez le et ajoutez une description si vous voulez puis "Create repository"
- Il faut maintenant relier votre repo Github à votre projet avec la commande que Github vous fournit `git remote add origin hhtps://github.com/votrenomgithub/nomdurepo.git` que vous entrez dans votre terminal à la racine de votre projet sur votre ordinateur après avoir d'abord initialisé GIT dans ce même projet avec `git init` comme expliqué [plus haut](#init)
- Vous pouvez maintenant effectuer votre premier commit (add vos fichiers puis commit)
- Ensuite il ne reste plus qu'à push le commit sur le repo Github avec la commande suivante `git push origin master` (ça pourrait être un autre nom que master si vous êtes sur une autre branche)
- Votre projet est maintenant sur votre repo (dépôt) Gitub
- Vous pouvez depuis votre repo récupérer toutes les version de votre code 
- Vous pouvez aussi récupérer les changements qui ont été push sur le repo (par un autre dev par exemple) avec la commande `git pull`

### 12 - README <a name='readme'></a>

- C'est un fichier .md (markdown) qui doit nous permettre d'écrire une documentation de notre projet
- Il suffit simplement de créer un fichier README.md à la racine de notre projet

### 13 - git clone <a name='clone'></a>

- Depuis votre repo vous avez accès à un lien "clone" que vous pouvez utiliser pour cloner votre projet sur votre ordinateur
- Il suffit de taper `git clone htps://github.com/votrenomgithub/nomdurepo.git` à l'endroit ou vous souhaitez cloner le projet
