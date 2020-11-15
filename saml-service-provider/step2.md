- Les fichiers de configuration par défaut installés au 1er lancement ne permettent pas le bon fonctionnement du provider SAML. Il faut maintenant les modifier pour ajouter votre configuration SAML particulière. Dans une configuration simple, il suffit de modifier le fichier application-saml.yaml.


Voici la liste des paramètres à modifier :

- keystore: "config/keystore-gar.jks" : préciser les certificats qui seront utilisés pour la création des métadonnées SAML de votre service provider.


cat << EOF >> /root/config/application-saml.yaml
saml:
  keyManager:
    keystore: "config/keystore-gar.jks"
    password: "gar"
    key:
      name: "gar"
      password: "gar"
  idp:
    metadata: "https://idp-auth.validation.test-gar.education.fr/idp/metadata"
  metadata:
    entityId: "https://gar-grt-validation-saml.pubqlf.co.as8677.net/saml/metadata"
EOF
```{{execute}}


Vérifier le contenu du fichier modifié :

`cat /root/config/application-saml.yaml`{{execute}}



