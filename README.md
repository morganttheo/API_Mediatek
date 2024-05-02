# rest_mediatekdocuments
Cette API est utilisée par l'application MediatekDocuments écrite en C# et récupérable dans le dépôt suivant :<br>
https://github.com/morganttheo/Application_Mediatek<br>
Le readme présente l'application et aussi le rôle de l'API.
## Présentation
Cette API, écrite en PHP, permet d'exécuter des requêtes SQL sur la BDD Mediatek86 créée avec le SGBDR MySQL.<br>
Elle est accessible via une authentification "basique" (avec login="admin", pwd="adminpwd").<br>
Sa vocation actuelle est de répondre aux demandes de l'applicaton MediatekDocuments.
## Fichiers de l'API
Cette API contient les fichiers suivants :<br>
- .htaccess : contient les règles de réécriture pour l'accès à mediatekdocuments.php avec les bons paramètres.<br>
- Mediatekdocuments.php : point d'entrée de l'api, contrôle l'accès sécurisé, récupère les paramètres puis, suivant le verbe utilisé (GET, POST, PUT, DELETE), appelle la méthode concernée dans la classe Controle.<br>
- Controle.php : suivant les demandes, appelle les méthodes concernées dans la classe AccesBDD puis retourne le résultat au format json.<br>
- AccesBDD.php : construit les requêtes SQL avec les collections de paramètres, demande à la classe ConnexionPDO de les exécuter et retourne le résultat.<br>
- ConnexionPDO.php : se connecte à la BDD, construit les requêtes en intégrant les paramètres, les exécute et retourne le résultat.
