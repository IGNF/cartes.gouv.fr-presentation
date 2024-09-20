Dans la suite on ne parle que de la brique d'alimentation et de diffusion.

Et même uniquement de l'espace connecté.

En faisant le lien avec les concepts de l'API manipulés.

---

## Le tableau de bord

![Tableau de bord](images/tableau-de-bord.png)

------

### Mon compte

![Accès à Mon compte](images/card-mon-compte.png)

Une seule requête à l'API Entrepôt :

```swagger
GET /users/me
```

Cette page permet de retrouver son identifiant technique si le support vous le demande et d'avoir le lien pour [modifier son compte Géoplateforme](https://sso.geopf.fr/realms/geoplateforme/account/).

------

### Mes clés d'accès

Pour créer des clés d'accès à partir des permissions qui nous sont accordées.

Par exemple les permissions d'accès aux données sous licence de l'IGN (SCAN25, SCAN OACI...) ou celles d'autres producteurs.

------

#### Ajouter une clé : services accessibles

![Ajouter une clé étape 1](images/ajout-cle-etape-1.png)

------

#### Ajouter une clé : options de sécurisation

![Ajouter une clé étape 2](images/ajout-cle-etape-2.png)

------

#### Consulter une clé

On peut modifier ou supprimer une clé existante et récupérer facilement le hash des clés de ce type.

![Détail clé de type HASH](images/cle-hash.png)
