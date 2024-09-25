
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

![Suivi des consommations Données Déposées](images/consommation-donnees-deposees.png)

------

![Suivi des consommations Données Déposées](images/consommation-endpoint.png)

------

* Seule interface où toutes les données sont visibles, notamment les téléversements ainsi que les données ou configurations qui ne sont pas liées à une fiche de données (pas de tag).
* La seule action possible est de supprimer (ou dépublier selon le cas) un objet

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

![Menu Permissions accordées](images/menu-permissions-accordees.png)

------

### Liste des permissions

Parmi les permissions de l'espace de travail il y a déjà les permissions créées automatiquement pour votre propre communauté à chaque publication d'un flux privé.

Vous pouvez les modifier ou les supprimer si elles ne vous conviennent pas. Elles ne servent à rien si aucune clé ne les utilise.

------

### Ajouter une permission

* un nom ou licence (visible par vous et les bénéficiaires)
* des bénéficiaires (plusieurs bénéficiaires => plusieurs permissions mais un seul formulaire de création)
* une date d'expiration (par défaut date du jour + 2 ans)
* le ou les service(s) concerné(s)
* si des clés oauth2 (authentification forte) sont obligatoires pour l'utiliser

------

NB : comme pour la gestion des membres de la communauté, on ne peut pas lister d'utilisateurs ici. Pour donner une permission personnelle, il vous faut connaitre l'identifiant du compte personnel.

On liste par contre les communautés dont vous avez connaissance :

* celles dont vous êtes membre
* celles qui sont listées dans le catalogue des communautés publiques