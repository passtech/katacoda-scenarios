

Les fichiers de configuration par défaut installés (application.yaml et application-saml.yaml) doivent être modifiés pour permettre le bon fonctionnement du provider SAML. 
Dans une configuration simple, uniquement le fichier application-saml.yaml doit être modifié


Voici la liste des paramètres à modifier :

   - **keystore** : "config/keystore-gar.jks" : Le keystore permet de préciser les certificats qui seront utilisés pour la création des métadonnées SAML de votre service provider. Il doit contenir une clé privé.
   Le keystore est lisible par l'application uniquement avec un mot de passe.

   Le keystore peut contenir plusieurs certificats. Il est nécessaire de préciser un nom de clé et un password pour l'ouvrir (paramètre key: name et key: password) 

   - **idp** : La protection SAML peut fonctionner avec différents IDP (Identity provider). Dans cette exemple, celui de l'environnement de test est utilisé.

   - **metadata** : entityId: C'est un identifiant permettant de préciser l'identité de votre fournisseur de services SAML auprès de l'IDP

   - **samlProxy** : ces paramètres indiquent le site Web à protéger


Ces paramètres sont disponibles à la fin du fichier application-saml.yml

`tail -23 /root/config/application-saml.yml`{{execute}}



```
saml:
  keyManager:
    keystore: "config/keystore-gar.jks"
    password: "gar"
    key:
      name: "gar"
      password: "gar"
  idp:
    metadata: "https://idp-auth.dev.test-gar.education.fr/idp/metadata"
  metadata:
    entityId: "https://dev-saml-service-provider.tech.fr/saml/metadata"
  samlProxy:
    scheme: http
    serverName: localhost
    serverPort: 9090
    includeServerPortInRequestURL: true
    contextPath: /
```





