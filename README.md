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

### Découvrir l'univers de Ruby en voyageant sur de bonnes Rails 

Regardez l'architecture du projet.
Vous devriez voir plusieurs fichiers et dossiers, dont les principaux:
- app: Contient principalement les contrôleur, les vues, les modèles et les assets de l'application
- config: Contient les fichiers de cnofiguration relatifs à l'application
- db: Contient tout ce qui permet de construire la base de donnée
- Gemfile: Contient la liste des plug-ins déjà existants qui vont etre utilisés dans l'application

Si vous ouvrez le dossier ````app````, vous découvrirez les dossiers suivants:
- contrôleur (controllers) : Ils réagissent aux actions des utilisateurs et vont chercher les données dans la base (grace aux modèles) pour les mettre à disposition des vues.
- modèles (models) : Ce sont des objets assurant la gestion des données.
- vues (views) : Elles correspondent à la manière d'afficher les informations à l'utilisateur. Il s'agit généralement d'une combinaison de code HTML et de Ruby dans des fichiers .html.erb.
- assets: Ce sont les images, les morceaux de code javascript et les feuilles de style en CSS utilisés dans les vues.

Apres avoir navigué dans les différents dossiers, passons à la pratique !

### Ouvrir le contrôleur et la vue principaux de l'application

Nous allons manipuler deux fichiers dans cet exercie: le contrôleur Curiosites et la seule vue liée à ce controlleur.
Essayez de les trouver et ouvrez les avec votre éditeur de texte. 

Quelques notions:

Ruby On Rails permet d'utiliser au mieux le protocole HTTP, sur lequel repose la navigation web. Il y a 4 types de requêtes principales en HTTP : GET (afficher une page), POST (créer une nouvelle ressource), PATCH (modifier partiellement une ressource, ou PUT qui modifie entièrement la ressource) et DELETE (supprimer une ressource). Suite à chaque requête, le serveur envoie une réponse.

De plus, il y a 7 actions de base dans chaque contrôleur Rails, qui sont: 
- SHOW : affiche une ressource en particulier
- INDEX : affiche la liste de toutess les ressources d'un meme type
- NEW : affiche le formulaire pour créer une nouvelle ressource
- CREATE : une fois le précédent formulaire complété, crée la ressource
- EDIT : affiche le formulaire d’édition d'une ressource
- UPDATE : met a jour une ressource spécifiée 
- DESTROY : supprime une ressource spécifique

Petit indice: Le controlleur Curiosites n'a que l'action INDEX et la vue qui nous intéresse pour cet exercice est liée à cete action. 

### Lancer le serveur sur lequel va tourner l'application

En premier lieu, vérifiez que votre application a tous les plug-ins qu'elle utlise bien installés en faisant la commande ````bundle install````dans votre console, à l'interieur de votre projet ````week-3````. 

Si un probleme survient au niveau de la version de ruby, vous devriez avoir besoin d'effectuer la commande ````rbenv install 2.3.1```` dans la console pour installer la version de ruby dont l'application a besoin. 
(Si rbenv ne connait pas cette version, utilisez la commande ````brew update && brew upgrade ruby-build```` avant)
Puis, installez bundler pour cette version avec la commande ````gem install bundle````. Et enfin, faites un ````bundle update````pour mettre a jour vos plug-ins. 

Pour lancer un serveur Ruby On Rails, vous devez faire la commande ````rails server```` (ou ````rails s````) toujours dans votre console. 
Et voila, votre serveur est lancé !

### Visualiser l'application sur le navigateur

Apres avoir lancé votre serveur, vous pourrez ouvrir votre navigateur pour y coller l'url suivante: http://localhost:3000/
Vous devriez visualiser le contenu de la vue que vous avez ouverte précédement. 
Apres avoir fait des modifications sur cette vue, vous n'aurez qu'à recharger la page du navigateur pour voir vos modifications apparaitre. (rafraichir: ````CTRL + R```` sous windows ou ````CMD + R```` sous mac)

### Mettre à jour la vue pour afficher votre cabinet de curiosité

Vous avez trouvé le fichier HTML qui correspond à la vue du controlleur Curiosites. Bien joué ! 
Maintenant, il s'agit simplement de le modifier pour afficher la page de curiosités que vous avez mis en place. Apres cela, n'hésitez pas à regarder ce qui s'affiche sur votre navigateur !

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
- Le protocole HTTP: https://openclassrooms.com/courses/les-requetes-http
- Les actions CRUD: https://fr.wikipedia.org/wiki/CRUD
- Avoir une définition succinte de Ruby On Rails : https://fr.wikipedia.org/wiki/Ruby_on_Rails
- La documentation officielle de Ruby On Rails : http://guides.rubyonrails.org/
- Notions intéressantes Ruby On Rails : http://geekmeup.fr/les-10-avantages-de-ruby-on-rails-pour-apprendre-a-bien-coder/
- Rails is like Burger King, par Simon Courtois : http://fr.slideshare.net/happynoff/rails-king
