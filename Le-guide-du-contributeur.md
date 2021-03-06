# Le guide du contributeur

## Communications au sein de l'équipe
L'équipe communique principalement sur un serveur Discord, auquel vous pouvez demander d'être invité. Le wiki de Github centralise les diverses informations utiles pour participer au projet.  
Nous utilisons le wiki même (partie Fonctionnalités) pour récapituler les tâches principales en cours, et les issue Github sont utilisées afin de poser les problèmes ou améliorations futures relatifs à un dépôt individuel. 

## Les dépôts du projet
Le projet Ylinor s'articule principalement autour des différents dépôts de plugin appliqués au serveur. Ces derniers sont séparés par thèmes de fonctionnalités, et représentent les différents axes d'évolution sur lesquels mise l'équipe de développement.  

## Synchronisation Sonar
Des plugins Sonar et un [Sonarcloud](https://sonarcloud.io/organizations/ylinor-github/projects) sont utilisés dans le but d'effectuer de l'analyse de code et de pouvoir repérer les vulnérabilités ou mauvaises pratiques de développement.  
L'analyse Sonar est réalisée à chaque commit à l'aide de Travis.ci. Pour pouvoir vous aussi pousser sur le Sonarcloud depuis votre poste de développement, vous avez besoin de vous y connecter au moins une fois et de demander à l'un des membres du groupe ylinor-github de vous y ajouter.  
Une fois ajouté, vous aurez besoin d'avoir un clé/jeton (récupérable depuis votre profil) personnel Sonarcloud. Créez alors à la racine du dépôt souhaité un fichier "gradle.properties" contenant la ligne "systemProp.sonar.login=TOKEN". La tache Gradle sonarqube enverra alors les informations au Sonarcloud pour les branches configurées.
