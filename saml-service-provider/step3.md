Le conteneur contenant la protection SAML peut être maintenant démarré
 
 - Démarrer le conteneur 

`docker run -e SPRING_PROFILES_ACTIVE=saml -v /root/config:/app/config -p 80:8080 ghcr.io/passtech/saml-service-provider:1.1.0`{{execute}}

- Ouvrir l'url de l'application démarrée dans le container :

https://[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com