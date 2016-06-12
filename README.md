# Etape 1 : Récuperer le projet week-3

Ouvrez une console et entrez dans votre répertoire de travail (aidez vous des commandes ````cd```` (changement de dossier) et ````ls```` (listing des fichiers)).
Créez un nouveau dossier de travail (````mkdir````: make directory):
``` Console
mkdir week-3
````

Entrez dans ce dossier:
``` Console
cd week-3
````

Initialisez GIT pour votre projet:
``` Console
git init
````
Vous allez maintenant lier votre répertoire ````week-3```` situé sur votre ordinateur avec un répertoire distant week-3 situé sur votre compte github. Le lien sera appelé ````origin````.
Pour cela, créez un nouveau répertoire appelé ````week-3```` sur Github et copiez l'url de ce répertoire.
Puis, faites la commande suivante, en remplaçant l'url par la votre:
``` Console
git remote add origin git@github.com:(votre compte)/week-3.git
````
Cela vous permet de synchroniser votre compte github avec les modifications que vous ferez sur le projet week-3 sur votre ordinateur.

A cette étape, si vous faites ````ls```` dans votre console, le dossier ````week-3```` doit etre vide.

Maintenant, vous allez lier votre répertoire ````week-3```` situé sur votre ordinateur avec le répertoire distant ````week-3```` situé sur le compte des Women On Rails. Le lien sera appelé ````upstream````. 
Pour cela, fites la commande suivante:
``` Console
git remote add upstream git@github.com:women-on-rails/wow-curiosites-1.git
````
Cela va vous permettre de récupérer facilement le code existant nécessaire pour la suite de l'exercice. 

Pour récupérer ce code, faites la commande suivante:
``` Console
git pull upstream week-3_beginning
````

Cela remplit le dossier ````week-3```` sur votre ordinateur avec tout ce que contient le projet ````week-3```` sur le compte Github des Women On Rails. 
En faisant un ````ls````, vous pourrez voir la liste des fichiers copiés. 

Vous voila prete pour l'exercice !

# Etape 2: Lire l'exercice et se lancer

Ouvrez votre projet week-3 avec l'éditeur que vous utilisez. 
Si vous utilisez SublimeText, vous pouvez faire ````subl.```` dans la console pour ouvrir directement votre projet. 

Regardez l'architecture du projet.
Vous devriez voir plusieurs fichiers et dossiers, dont les principaux:
- app: Contient principalement les controlleurs, les vues, les modèles et les assets de l'application
- config: Contient les fichiers de cnofiguration relatifs à l'application
- db: Contient tout ce qui permet de construire la base de donnée
- Gemfile: Contient la liste des plug-ins déjà existants qui vont etre utilisés dans l'application

Si vous ouvrez le dossier ````app````, vous découvrirez les dossiers suivants:
- controlleurs (controllers) : Ils réagissent aux actions des utilisateurs et vont chercher les données dans la base (grace aux modèles) pour les mettre à disposition des vues.
- modèles (models) : Ce sont des objets assurant la gestion des données.
- vues (views) : Elles correspondent à la manière d'afficher les informations à l'utilisateur. Il s'agit généralement d'une combinaison de code HTML et de Ruby dans des fichiers .html.erb.
- assets: Ce sont les images, les morceaux de code javascript et les feuilles de style en CSS utilisés dans les vues.

Apres avoir navigué dans les différents dossiers, ouvrez le fichier 
- ouvrir fichier de travail (controller )
- lancer server 
- regarder sur le navigateur
- trouver le fichier html a chanegr pour afficher le cabinet de curiosité (copié collé)

# Etape 3: Enregistrer les modifications sur le répertoire distant

Lorsque vous avez fait des modifications dans votre projet ````week-2````, vous pouvez avoir besoin de les enregistrer pour ne pas les effacer malencontreusement. Pour cela, vous allez les 'committer'. 

Pour committer ces changements, vous devez d'abord les ajouter aux modifications à prendre en compte avec la commande:
``` Console
git add .
````

Si vous souhaitez ne prendre en compte que certaines modifications et pas d'autres, vous pouvez utiliser la commande:
``` Console
git add -p 
````
Cela vous permettra de visualier chaque modification et de l'ajouter (````y````) ou non (````n````). 

PS: Si vous voulez simplement visualiser les fichiers modifiés, faites:
``` Console
git status
````

Pour rendre l'enregistrement des modifications effectif, il faut faire la commande:
``` Console
git commit 
````

Si vous voulez décrire le contenu de votre commit, vous pouvez y ajouter une option:
``` Console
git commit -m "description blabla"
````
Cela permet de savoir rapidement à quoi correspond le commit, au lieu de regarder sa composition. 

Pour envoyer votre commit vers votre repertoire distant (sur Github), vous devez ensuite utiliser la commande ````push````:
```Console
git push 
````

Allez voir sur github, vos modifications apparaitront :)

# Pour aller plus loin:
- Avoir une définition succinte de Ruby On Rails : https://fr.wikipedia.org/wiki/Ruby_on_Rails
- L documentation officielle de Ruby On Rails : http://guides.rubyonrails.org/
