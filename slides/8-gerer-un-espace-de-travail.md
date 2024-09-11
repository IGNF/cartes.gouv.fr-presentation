
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



------

### Permissions accordées