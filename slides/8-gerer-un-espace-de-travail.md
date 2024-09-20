
## Gérer son espace de travail

* Gérer les membres de la communauté
* Suivre les consommations
* Accorder des permissions

------

### Gérer les membres de la communauté

![Membres d'une communauté](images/membres.png)

------

```swagger
GET /communities/{community}/users
```

On retrouve la matrice des droits de l'API

```json
    "rights": [
      "PROCESSING",
      "UPLOAD",
      "ANNEX",
      "BROADCAST",
      "COMMUNITY"
    ],
```

💡 On ne peut pas modifier ses propres droits et ceux du superviseur.


------

#### Ajouter un utilisateur

![Membres d'une communauté](images/ajouter-un-utilisateur.png)

------

👍 L'identifiant de l'utilisateur est prérempli si on utilise le lien dans le mail reçu quand l'utilisateur a demandé à rejoindre la communauté... mais ça ne marche que pour les communautés publiques.

😅 Sinon il faut lui demander son identifiant qu'il peut copier-coller sur sa page `/mon-compte`

------

### Suivi des consommations

![Menu Suivi des consommations](images/menu-suivi-des-consommations.png)

------

* Seule interface où toutes les données sont visibles, notamment les téléversements ainsi que les données ou configurations qui ne sont pas liées à une fiche de données (pas de tag).
* La seule action possible est de supprimer (ou dépublier selon le cas) un objet

------

![Suivi des consommations Données Déposées](images/consommation-donnees-deposees.png)

------

![Suivi des consommations Données Déposées](images/consommation-endpoint.png)

------

⚠️

On trouve quelques objets techniques parmi les annexes :

* des fichiers de getcapabilities filtrés
* des listes de documents
* des fichiers de styles

Ne supprimez rien à la légère !

Lorsque l'objet porte un nom de fiche de données, mieux vaut passer par les interfaces de la fiche de données pour faire le ménage.

------

### Permissions accordées

🏗️