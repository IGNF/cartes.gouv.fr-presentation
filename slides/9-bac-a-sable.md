## Le bac à sable

![Espace Découverte sur le tableau de bord](images/decouverte-sur-tableau-de-bord.png)

------

* La communauté s'appelle **Découverte**
* Tous les utilisateurs sont automatiquement ajoutés comme membre grâce à un compte de service qui possède les seuls droits **COMMUNITY**
* Donc tout est partagé, le travail et les essais de tout le monde sont visibles et modifiables par tout le monde
* Et donc tout est périssable ⚠️

------

* L'entrepôt associé dispose de ses propres traitements, stockages et endpoints, similaires à ceux des entrepôts *normaux*, avec un petit `sandbox` en plus dans les urls.
  ```url
  https://data.geopf.fr/sandbox/wms-v
  ```

* Mais il n'y a pas de endpoints privés. Donc pas de possibilité de publier des flux en accès restreint

------

* On peut aller jusqu'à la publication des flux et des métadonnées et obtenir des URLs fonctionnelles
* On ne peut pas accéder à la liste des membres (pas de droit **COMMUNITY** par défaut)
* Les métadonnées ne sont accessibles que via le service CSW et ne sont pas référencées dans le catalogue