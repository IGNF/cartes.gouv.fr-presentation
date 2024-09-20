
## Obtenir un espace de travail

Un espace de travail = une communauté + un entrepôt

------

### Option 1 : Rejoindre un espace de travail existant

![Rejoindre un espace de travail existant](images/card-rejoindre-un-espace-de-travail.png)

Cette page liste les communautés publiques qui ont une adresse email de contact qui ressemble à un email.

------

Requête à l'API Entrepôt :

```swagger
GET /catalog/communities
```

------

Elle propose un formulaire de contact simple qui envoie un email à cette adresse de contact. Ce mail contient notamment vos informations, dont votre identifiant technique car il est nécessaire pour vous ajouter comme membre.

⚠️ cartes.gouv.fr ne conserve pas la trace des demandes. C'est entre vous et le responsable de la communauté concernée.

------

### Option 2 : Demander la création d'un espace de travail

![Demande de création d'un espace de travail](images/card-demande-de-creation-espace-de-travail.png)

Cette page est un formulaire de contact dédié pour que le support puisse vous créer une communauté et un entrepôt.

------

![Espace de travail neuf](images/espace-de-travail-vide.png)

Une fois l'accès à un espace de travail obtenu, on peut commencer à déposer des données et les publier !