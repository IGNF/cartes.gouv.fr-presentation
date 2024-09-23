## Publier en TMS

Tuiles vectorielles

------

On repart de l'étape ou on a déjà une base de données prête pour la création de nouveaux services

------

![Modale Créer un service](images/tms-nom-pyramide.png)

------

* avant de commencer on doit choisir un nom pour la `stored_data` pyramide qui va être générée
* **étape 1** : on choisit les tables à conserver dans la pyramide
* **étape 2** : on choisit explicitement les attributs de chaque table à conserver dans la pyramide. Moins il y a d'attributs, plus la généralisation est efficace
* **étape 3** : on choisit les niveaux de la pyramide à générer. Ou sur quels niveaux de la pyramide doivent apparaitre quelles données

------

![Génération de pyramide : choix des bornes de zoom](images/tms-niveaux-de-zoom.png)

------

💡 Pour se faire une idée de la taille des tuiles à différents niveaux : https://rok4.github.io/#visualisation-du-quadrillage

------

* **étape 4** : des options préconfigurées de généralisation qui vont être plus ou moins adaptés à certains types géométriques mais dont l'efficacité va dépendre également des choix précédents
  
  Objectif : qu'il y ait quelque chose à montrer aux petites échelles de pas trop moche et sans que chaque tuile soit trop lourde à charger

------

![Génération de pyramide : choix du type de généralisation](images/tms-choix-generalisation.png)

------

La généralisation de la pyramide peut prendre du temps. Si vos données sont très volumineuses il est possible de créer d'abord un échantillon (**étape 5**), c'est à dire une pyramide sur une zone limitée, pour valider la pertinence de vos choix. Le calcul de cet échantillon sera plus rapide car moins de tuiles seront générées aux grandes échelles.

------

![Génération de pyramie : choix de la zone d'échantillon](images/tms-zone-echantillon.png)

------

### Publier le service

Une fois la pyramide générée, vous aurez un bouton pour **Publier le service TMS**

La publication reprend les étapes de remplissage des métadonnées (déjà remplies 👍, faire juste attention au **nom technique du service**) et le choix de publier en public ou en accès restreint.

------

### Cas de l'échantillon

L'échantillon est publié automatiquement pour que vous puissiez le visualiser et s'il vous convient vous avez un accès direct à la génération de la pyramide complète sur l'ensemble de l'emprise de vos données.

------

### Ajouter des styles (facultatif)

S'agissant d'un flux de données vecteur, comme pour le WFS, l'application d'un style est optionnelle car elle se fait côté client.

En plus du SLD et du QML, vous pouvez utiliser le format de fichier JSON aux spécifications Mapbox Style, plus adapté à ce format.