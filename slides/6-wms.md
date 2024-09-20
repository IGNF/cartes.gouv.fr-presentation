## Publier en WMS

WMS dit "vecteur", c'est-à-dire généré à la volée

------

On repart de l'étape ou on a déjà une base de données prête pour la création de nouveaux services et on clique également sur **Créer un service**

------

![Modale Créer un service](images/modale-creer-un-service.png)

------

Ouh là là c'est encore plus long que le WFS 😱

![Tunnel WMS en 6 étapes](images/wms-6-etapes.png)

------

### Déposer un fichier de style

![Déposer un fichier de style pour WMS](images/wms-depot-sld.png)

Les messages d'erreur vous guident pour modifier votre SLD (seul format possible). Ce fichier sera déposé comme fichier statique.

------

### Les métadonnées...

Pareil que pour le WMS, il faut un nom pour le service (ne gardez pas celui par défaut, il est pas terrible)

✨ Et tout le reste est déjà rempli ! ✨ 

------

![Fiche de données, onglet services avec un service WFS et un service WMS](images/fiche-de-donnees-service-wfs-et-wms.png)

On a une nouvelle configuration, une nouvelle offre et une métadonnée actualisée avec une 2<sup>ème</sup> URL de service.

------

![Visualisation WMS](images/wms-previsualisation.png)

------

* L'affichage est déjà plus rapide que le WFS mais les images demandées sont générées à la volée, il n'y a pas encore de tuiles pré-calculées.

* Si vous voulez changer de style, il faut publier un autre service WMS. Les services WMS ne sont pas personnalisables côté client.
