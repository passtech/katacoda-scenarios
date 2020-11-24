Le conteneur utilise des fichiers de configuration dans le répertoire config.
Si le répertoire config ne contient pas de fichier, il installe une configuration par défaut qu'il faut modifier.

 - Créer un répertoire config. Dans notre espace de test Katacoda, le répertoire est créé sous /root

`mkdir config`{{execute}} 

 - Changer les droits pour permettre la création des fichiers de configuration par Docker lors du 1er lancement

`chmod 777 config`{{execute}}

- 3 fichiers de configurations nécessaires à l'application dans le répertoire config précédemment créé sont téléchargés à partir de Github et copiés dans le répertoire config.

`wget https://raw.githubusercontent.com/passtech/katacoda-scenarios/master/saml-service-provider/files/application.yml -O /root/config/application.yml`
`wget https://raw.githubusercontent.com/passtech/katacoda-scenarios/master/saml-service-provider/files/application-saml.yml -O /root/config/application-saml.yml`{{execute}}
`wget https://raw.githubusercontent.com/passtech/katacoda-scenarios/master/saml-service-provider/files/keystore-gar.jks -O /root/config/keystore-gar.jks`{{execute}}

`ls -al /root/config`{{execute}}

- Voir le contenu des fichiers 

`/root/config/application.yml`{{open}}

`/root/config/application-saml.yml`{{open}}




