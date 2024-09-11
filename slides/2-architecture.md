## Plusieurs briques

* Un portail et un back-office (espace connecté) d'alimentation et de diffusion
* Une entrée cartographique qui deviendra à terme la page d'accueil et remplacera l'actuel [geoportail.gouv.fr](https://geoportail.gouv.fr)
* Un catalogue public
* 🔜 Un site statique de documentation (en cours de construction)

------

### Brique Alimentation/Diffusion

https://cartes.gouv.fr

Site basé sur Symfony et [codegouvfr/react-dsfr](https://github.com/codegouvfr/react-dsfr)

Code source : [IGNF/cartes.gouv.fr](https://github.com/IGNF/cartes.gouv.fr)

![License: AGPL-3.0](https://img.shields.io/badge/License-AGPL--3.0-blue.svg)

------

### Entrée carto

https://cartes.gouv.fr/cartes/

Single Page App basée développée en [Vue](https://vuejs.org/) et utilisant les [extensions Géoplateforme pour OpenLayers](https://github.com/IGNF/geopf-extensions-openlayers).

Code source : [IGNF/cartes.gouv.fr-entree-carto](https://github.com/IGNF/cartes.gouv.fr-entree-carto)

![License: AGPL-3.0](https://img.shields.io/badge/License-AGPL--3.0-blue.svg)

------

### Catalogue

https://cartes.gouv.fr/catalogue/

Site basé sur [Datahub (aka. geonetwork-ui)](https://github.com/geonetwork/geonetwork-ui)

Code source : [IGNF/geonetwork-ui](https://github.com/IGNF/geonetwork-ui)

![License: GPL-2.0](https://img.shields.io/badge/License-GPL--2.0-blue.svg)

------

### Documentation

https://cartes.gouv.fr/documentation/ (non déployée)

Site statique généré à partir de contenus en markdown avec [eleventy](https://www.11ty.dev/) et des gabarits basés sur [eleventy-dsfr](https://github.com/codegouvfr/eleventy-dsfr).

Code source : [IGNF/cartes.gouv.fr-documentation](https://github.com/IGNF/cartes.gouv.fr-documentation)

![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)