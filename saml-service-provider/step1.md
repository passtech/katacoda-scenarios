# Installation

Le conteneur utilise des fichiers de configuration dans le répertoire config.
Si le répertoire config ne contient pas de fichier, il installe une configuration par défaut qu'il faut modifier.

 - ### Créer un répertoire config. Dans notre espace de test Katacoda, le répertoire est créé sous /root

`mkdir config`{{execute}} 

 - ### Changer les droits pour permettre la création des fichiers de configuration par Docker lors du 1er lancement

`chmod 777 config`{{execute}}

- ### Installer les fichiers de configurations nécessaires à l'application dans le répertoire config précédemment créé



 - ### Démarrer le conteneur 

`docker run -e SPRING_PROFILES_ACTIVE=saml -v /root/config:/app/config -p 80:8080 ghcr.io/passtech/saml-service-provider:1.1.0`{{execute}}

- ### Ouvrir l'url de l'application démarrée dans le container :

https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com


