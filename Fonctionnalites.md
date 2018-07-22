# Fonctionnalités

Pour cette première phase de développement, quatre plugins ont été conçus.  
Ils peuvent chacun s'interconnecter, mais également être indépendants s'ils n'ont pas la possibilité de communiquer les uns avec les autres.  


## Première itération
Voici, pour chacun des quatre plugins, les premiers objectifs sélectionnés à court terme.


### Brawlator
Le plugin Brawlator concerne le combat et les créatures hostiles de manière générale.  

* Faire apparaître un monstre aux caractéristiques définies en commande Minecraft :heavy_check_mark:
* Stocker un monstre aux caractéristiques précises dans un fichier de configuration :heavy_check_mark:
* Donner des équipements et des effets de potions à un monstre à faire apparaître :heavy_check_mark:
* Stocker les objets et effets de potions à donner aux monstres dans un fichier de conf. :heavy_check_mark:
* Créer un système de spawner de monstres définis dans un fichier de conf. :heavy_check_mark:


### Itemizer
Le plugin Itemizer comprend la génération d'objets complexes.

* Créer un objet en lui attribuant une description (avec couleurs), des caractéristiques et des enchantements :heavy_check_mark:
* Stocker des objets complexes dans un fichier de configuration et les récupérer pour les créer :heavy_check_mark:
* Générer un objet aléatoirement parmi une liste d'objets définis :heavy_check_mark:

Le plugin Itemizer permet aussi de personnaliser les craft possibles.

* Ajouter un pattern de craft personnalisé :heavy_check_mark:
* Stocker ce pattern de craft dans un fichier de configuration :heavy_check_mark:


### Harvester
Le plugin Harvester gère la récolte de ressources.

* Restreindre les blocs minables à ceux définis dans un fichier de configuration :heavy_check_mark:
* Restreindre les blocs minables selon leurs variantes :heavy_check_mark:
* Modifier les récoltes de blocs minables en fonction de la configuration :heavy_check_mark:
* Utiliser des objets d'Itemizer dans les récoltes de Harvester :heavy_check_mark:

### Storyteller
Le plugin Storyteller gère les interactions avec les NPC donneurs de quêtes.

* Afficher une interface de livre avec un contenu prédéfini lors de l'interaction avec un NPC :heavy_check_mark:
* Y implémenter des boutons effectuant des actions telles que ouvrir un autre dialogue ou se téléporter :heavy_check_mark:
* Stocker les dialogues et leurs caractéristiques dans un fichier de configuration :heavy_check_mark:
* Stocker la progression des quêtes dans une base de données SQLite :heavy_check_mark:
* Utiliser la progression en tant que condition et qu'action des dialogues :heavy_check_mark:

## Deuxième itération
Ci-dessous les objectifs de la seconde itération de développement.

### CrowdBinding
Le plugin CrowdBinding aggrémente le serveur de fonctions sociales en tout genre.

* Permettre aux joueurs de créer un groupe en invitant un autre joueur :x:
* Afficher si possible les joueurs d'un groupe dans le scoreboard :x:
* Ajouter des commandes de gestion de groupe (quitter, exclure, coordonnées, ...) :x:
* Permettre les messages de groupe :x:
* Gérer la persistance des groupes ? (déco-reco) :x:

### EpicBoundaries
Le plugin EpicBoundaries se charge des intéractions avec le monde tels que la génération d'instance et l'utilisation de clés

* Etudier la possibilité d'ouvrir une porte / un coffre pour un unique joueur :x:
* Gérer un système de clés qui permet d'ouvrir des portes pour un joueur uniquement :x:
* Etudier la possibilité de gérer les instances :heavy_check_mark: (note : doit être testé en conditions de recette)
