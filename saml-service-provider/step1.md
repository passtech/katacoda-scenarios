# Installation

Le conteneur utilise des fichiers de configuration dans le répertoire config.
Si le répertoire config ne contient pas de fichier, il installe une configuration par défaut qu'il faut modifier.

 - Démarrer le conteneur 

`docker run -e SPRING_PROFILES_ACTIVE=saml -v /mnt/ssd/Workspace-PassTech/gar/saml-service-provider/config:/app/config -p 8080:8080 ghcr.io/passtech/saml-service-provider:1.1.0`{{execute}}

- Modifier les paramètres de configuration 


