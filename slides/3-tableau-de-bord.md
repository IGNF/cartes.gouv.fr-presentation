## Préambule

Dans la suite seule la **brique d'alimentation et de diffusion** est décrite.

Et même uniquement l'espace connecté.

En faisant le lien avec les concepts de l'**API Entrepôt** manipulés.

---

## Le tableau de bord : accueil de l'espace connecté

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

Pour créer des **clés d'accès** à partir des **permissions** qui vous sont accordées.

Par exemple les permissions d'accès aux données sous licence de l'IGN (SCAN25, SCAN OACI...) ou celles d'autres producteurs.

------

#### 2 onglets : Clés et permissions

![Page clés d'accès et permissions](images/onglets-cles-permissions.png)
------

Pour afficher les **clés d'accès** :

```swagger
GET /users/me/keys
GET /users/me/keys/{key}
```

Pour afficher les **permissions** :

```swagger
GET /users/me/permissions
GET /users/me/permissions/{permission}
```

------

#### Ajouter une clé : services accessibles

![Ajouter une clé étape 1](images/ajout-cle-etape-1.png)

------

#### Ajouter une clé : options de sécurisation

![Ajouter une clé étape 2](images/ajout-cle-etape-2.png)

------

#### Consulter une clé

Il est possible de modifier ou supprimer une clé et de copier le hash des clés de ce type.

![Détail clé de type HASH](images/cle-hash.png)

[data.geopf.fr/private/wmts?REQUEST=GetCapabilities&SERVICE=WMTS&VERSION=1.0.0&apikey=zxY1Tm7D02xNCGPJfE4VqDhQ6Vfdq7xU](https://data.geopf.fr/private/wmts?REQUEST=GetCapabilities&SERVICE=WMTS&VERSION=1.0.0&apikey=zxY1Tm7D02xNCGPJfE4VqDhQ6Vfdq7xU)

------

#### Manipulation d'une clé via l'API

Création

```swagger
  POST /users/me/keys
  POST /users/me/keys/{key}/accesses
```

Modification

```swagger
  PATCH /users/me/keys/{key}
  POST /users/me/keys/{key}/accesses
  DELETE /users/me/keys/{key}/accesses
```
Suppression
  
```swagger
  DELETE /users/me/keys/{key}
```

Explications détaillées : [Tutoriel de Gestion des clés](https://geoplateforme.github.io/tutoriels/production/controle-des-acces/diffusion/cle/)
