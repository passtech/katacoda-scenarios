# Installation

Le conteneur utilise des fichiers de configuration dans le répertoire config.
Si le répertoire config ne contient pas de fichier, il installe une configuration par défaut qu'il faut modifier.

 - Créer un répertoire config. Dans notre espace de test Katacoda, le répertoire est créé sous /root

`mkdir config`{{execute}} 

 - Changer les droits pour permettre la création des fichiers de configuration par Docker lors du 1er lancement

`chmod 777 config`

 - Démarrer le conteneur 

`docker run -e SPRING_PROFILES_ACTIVE=saml -v /root/config:/app/config -p 8080:8080 ghcr.io/passtech/saml-service-provider:1.1.0`{{execute}}

TODO : Ouvrir l'url  http://localhost:8080/error.html

