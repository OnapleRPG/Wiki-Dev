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
* Stocker ce pattern de craft dans un fichier de configuration :x:


### Harvester
Le plugin Harvester gère la récolte de ressources.

* Restreindre les blocs minables à ceux définis dans un fichier de configuration :heavy_check_mark:
* Restreindre les blocs minables selon leurs variantes :heavy_check_mark:
* Modifier les récoltes de blocs minables en fonction de la configuration :heavy_check_mark:
* Utiliser des objets d'Itemizer dans les récoltes de Harvester :heavy_check_mark:
