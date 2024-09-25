## Publier en WFS

Flux de données vecteur

------

![Créer une fiche de données](images/creer-une-fiche-de-donnees.png)

------

⚠️

* Le concept de fiche de données n'existe pas dans l'API Entrepôt
* Le nom de la fiche est une étiquette que *cartes.gouv.fr* ajoute à toutes les entités (`upload`, `stored_data`, `configuration`...) pour les regrouper en un ensemble cohérent qui correspondra, après la première publication, à une fiche catalogue.

------

Précisions sur le dépôt du fichier

![Déposer votre fichier](images/deposer-votre-fichier.png)

------

Dépôt en cours en 4 étapes successives côté API :

* Nouvel `upload`
* Vérifications standard (lancées automatiquement)
* Vérifications vecteur (lancées automatiquement)
* Intégration en base (traitement exécuté une fois l'`upload` prêt)

------

![Etapes de dépôt d'un fichier vecteur](images/integration-en-base.png)

...ça peut prendre quelques minutes

Si vous quittez ici, vous pourrez éventuellement revenir à votre fiche de données et cliquer sur "reprendre l'intégration"

------

Si tout va bien vous aboutissez à une fiche de données avec une base de données vecteur (une `stored_data` pour l'API) associée

![Fiche de données avec une base](images/fiche-de-donnees-jeux.png)

------

De là vous pouvez **Créer un service**

![Modale Créer un service](images/modale-creer-un-service.png)

------

Certaines options peuvent être désactivées ⁉️
* si le *quota* pour ce type de service est atteint sur les 2 *endpoints* (public et accès restreint)
* si le *quota* sur le *endpoint* pour les métadonnées est atteint

------

Et c'est parti pour 5 étapes 😱

![Tunnel de publication WFS](images/tunnel-wfs.png)

------

![Choix des tables à publier](images/tables-wfs.png)

Il n'est pas obligatoire de sélectionner toutes les tables

------

![Fichier de métadonnées](images/fichier-metadonnees-wfs.png)

🏗️

(ignorer l'étape, ce n'est pas fonctionnel)

------

### Les métadonnées

C'est LE morceau compliqué à remplir.

Presque tout est obligatoire, c'est ce qui va permettre à votre service d'être découvrable sur le catalogue.

C'est à remplir uniquement pour le premier service de votre fiche de données. Vous retrouverez la plupart des champs déjà remplis lors de la publication d'autres services 👍

------

Seul le premier champ n'est pas vraiment un champ de métadonnées, c'est le nom du service (typeName en WFS = `nom_du_service:nom_de_la_table`) qui sera utilisé dans les requêtes au service et visible dans le `GetCapabilities`.

![Nom technique du service](images/nom-technique-existant.png)

Si ce nom est déjà utilisé, vous êtes prévenu tout-de-suite.

------

![Publication publique ou privée](images/acces_wfs.png)

Une des options peut-être désactivée si vous avez atteint le quota du endpoint associé ou si ce endpoint n'est pas associé à votre entrepôt.

------

🚀

La publication elle-même est rapide. C'est la déclaration d'une `configuration` et d'une `offering` ainsi que la création et la publication d'une `metadata`.

------

![Fiche de données, onglet services avec un service WFS](images/fiche-de-donnees-service-wfs.png)

Si le service apparait bien *publié*, on peut le visualiser.

(Enfin une 🗺️ !)

------

![Visualisation WFS](images/visualisation-wfs.png)

⚠️ aux performances d'affichage à des niveaux de zoom pas forcément adaptés à vos données

------

### Ajouter des styles (facultatif)

Pas d'interface graphique avancée à ce jour, il faut préparer des fichiers sld ou qml

![Ajout d'un style pour WFS](images/ajout-style-wfs.png)

------

Et vérifier le rendu sur la visualisation

![Visualisation WFS avec un style](images/visualisation-wfs-avec-style.png)

------

Les fichiers de style sont enregistrés en tant qu'**annexes** et la métadonnée est modifiée pour y faire référence.

Vous trouverez aussi une annexe technique `styles.json` qui relie les couches et les styles individuels et permet l'affichage de cette visualisation.

------

### Cas des flux privés 🔒

Pas de visualisation possible car il faut s'être attribué une **permission** puis avoir configuré une **clé d'accès** qui exploite cette permission.

La publication créé une permission pour votre communauté, ce qui facilite la procédure. Mais elle ne créé pas ou ne modifie pas de clé. Il vous reste cette étape à faire pour pouvoir ensuite visualiser le service dans un SIG par exemple.

La métadonnée sera publique et visible sur le catalogue même si les flux eux-même sont privés.
