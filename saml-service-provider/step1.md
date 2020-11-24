Le conteneur utilise des fichiers de configuration dans le répertoire config.
Si le répertoire config ne contient pas de fichier, il installe une configuration par défaut qu'il faut modifier.

 - Créer un répertoire config. Dans notre espace de test Katacoda, le répertoire est créé sous /root

`mkdir config`{{execute}} 

 - Changer les droits pour permettre la création des fichiers de configuration par Docker lors du 1er lancement

`chmod 777 config`{{execute}}

- 2 fichiers de configurations nécessaires à l'application dans le répertoire config précédemment créé sont téléchargés à partir de Github et copiés dans le répertoire config.

`ls -al /root/config`{{execute}}
 
`/root/config/application.yml`{{open}}

`/root/config/application-saml.yml`{{open}}




