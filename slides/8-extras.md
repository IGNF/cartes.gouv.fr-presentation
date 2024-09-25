## Extras

Ajouter des documents et une vignette dans les métadonnées et autres particularités de fonctionnement

------

### Ajouter une vignette

![Bouton ajouter une vignette](images/bouton-ajout-vignette.png)

------

![Modale d'ajout de vignette](images/modale-ajout-vignette.png)

------

Ajoute une **annexe** taguée :
* *vignette*
* au nom de la fiche

![Vignette dans la consommation](images/vignette-dans-la-consommation.png)

------

Complète la métadonnées d'un bloc *graphicOverview* qui rend la vignette **visible dans le catalogue public** 🤩

```xml
<gmd:graphicOverview>
    <gmd:MD_BrowseGraphic>
        <gmd:fileName>
            <gco:CharacterString>
            https://data.geopf.fr/annexes/sandbox/thumbnail/a34d495b-357d-4c9e-a285-fbfdc92bc704.png
            </gco:CharacterString>
        </gmd:fileName>
        <gmd:fileDescription>
            <gco:CharacterString>Aperçu</gco:CharacterString>
        </gmd:fileDescription>
        <gmd:fileType>
            <gco:CharacterString>png</gco:CharacterString>
        </gmd:fileType>
    </gmd:MD_BrowseGraphic>
</gmd:graphicOverview>
```

------

### Documents

![Onglet documents d'une fiche de données](images/onglet-documents.png)

Vous pouvez ajouter des documents de tous types à vos métadonnées : tutoriels, documentations techniques, spécifications...

------

Si le document est déjà disponible sur internet :

![Ajouter un document URL externe, il faut donner un nom, une description, l'url et optionnellement une description](Images/ajouter-un-document-lien.png)

------

Comme pour la vignette, c'est un ajout dans les métadonnées :

```xml
<gmd:onLine type="document">
    <gmd:CI_OnlineResource>
        <gmd:linkage>
            <gmd:URL>https://www.youtube.com/watch?v=dQw4w9WgXcQ</gmd:URL>
        </gmd:linkage>
        <gmd:name>
            <gco:CharacterString>Tutoriel</gco:CharacterString>
        </gmd:name>
        <gmd:description>
            <gco:CharacterString>Comment utiliser le service</gco:CharacterString>
        </gmd:description>
    </gmd:CI_OnlineResource>
</gmd:onLine>
```

------

Si le document n'a pas d'URL publiquement accessible, alors on peut le téléverser

![Ajouter un document fichier](Images/ajouter-un-document-fichier.png)

------

On créé alors une nouvelle **annexe** et c'est l'url de cette annexe qui est utilisée dans les métadonnées. Donc une URL qui commence par `https://data.geopf.fr/annexes/{community}/...`


------

### Supprimer tous les services

Lorsque vous supprimez tous les services d'une fiche sans supprimer la fiche elle-même, la métadonnée est conservée mais n'est plus publiée (plus visible sur le catalogue).

Ceci permet de revenir plus facilement sur les formulaires de publication déjà pré-remplis des étapes métadonnées.
