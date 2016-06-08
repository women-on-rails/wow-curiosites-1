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
