---
description: Metadati XMP. Restituisce i metadati XMP associati all'immagine specificata nel percorso della richiesta.
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 91e252dd-22e2-4c4e-bc92-67762114c2ce
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# xmp{#xmp}

Metadati XMP. Restituisce i metadati XMP associati all&#39;immagine specificata nel percorso della richiesta.

`req=xmp`

Altri comandi vengono ignorati. Si applica la codifica UTF-8. La risposta viene formattata come XML con il tipo MIME `text/xml`.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::Expiration`.

## Proprietà {#section-0d26b6a56c844153ae5cea4880370d00}

Attributo di richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente.

## Predefinito {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

Se l&#39;URL non include un percorso immagine o modificatori, allora:

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

In caso contrario, `req=img`

## Esempi {#section-34213692deab4a0f9037d5844132ee14}

Proprietà del file immagine della query.

` http:// *`server`*/myPath/myImage.tif?req=imageprops`

Proprietà catalogo immagini query:

` http:// *`server`*/myRootId?req=catalogprops`

Accedi alle proprietà di una voce di catalogo immagini da JavaScript lato client incorporato in un file HTML:

```
<script language="JavaScript"> 
     //req=imageprops populates this object with properties: 
     var image = new Object; 
</script> 
<script src="http://server/myRootId/myImageId?req=imageprops,javascript"></script> 
<script> 
     alert("Image Size: " + image.width + " x " + image.height); 
</script>
```

Recupera l&#39;immagine della maschera per una particolare voce di catalogo, ridimensionata al 25% della dimensione originale:

` http:// *`server`*/myRootId/myImageId?req=mask&scale=0.25`

Richiedi un&#39;immagine a una dimensione di un ottavo:

` http:// *`server`*/myRootId/myImageId?scl=8`

È lo stesso di:

` http:// *`server`*/myRootId/myImageId?req=img&scl=8`

Richiedi una miniatura di un’immagine, basandosi sugli attributi delle miniature specificati nel catalogo immagini:

` http:// *`server`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

Invia un messaggio di testo ai log del server:

` http:// *`server`*/myRootId?req=message&message=This%20is%20the%20message`

## Consultate anche {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ,  [catalogo::Target](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md),  [catalogo::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md),  [Ridimensionamento miniature](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f),  [Proprietà](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9), Mappe  [immagine](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
