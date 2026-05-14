---
description: Metadati di XMP. Restituisce i metadati XMP associati all’immagine specificata nel percorso della richiesta.
solution: Experience Manager
title: xmp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 91e252dd-22e2-4c4e-bc92-67762114c2ce
TQID: 'https://experienceleague.adobe.com/yPJzG9VRk975dHWzRc6o-OX5njAccH8CcwpR-J--uHk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 179
ht-degree: 1%

---

# xmp{#xmp}

Metadati di XMP. Restituisce i metadati XMP associati all’immagine specificata nel percorso della richiesta.

`req=xmp`

Gli altri comandi vengono ignorati. Si applica la codifica UTF-8. La risposta è formattata come XML con tipo MIME `text/xml`.

La risposta HTTP è memorizzabile in cache con TTL basato su `catalog::Expiration`.

## Proprietà {#section-0d26b6a56c844153ae5cea4880370d00}

Attributo della richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente.

## Predefinito {#section-1b2e089dce5d4e0ab664c62bf1be90dd}

Se l’URL non include uno o più modificatori di immagine, effettua le seguenti operazioni:

```
#S7Z OK 
#Mon Jul 25 17:28:32 PDT 2014 
copyright=Copyright (c) 1995-2014 Adobe Systems Incorporated. All rights reserved.
```

In caso contrario, `req=img`

## Esempi {#section-34213692deab4a0f9037d5844132ee14}

Eseguire una query sulle proprietà del file di immagine.

` http:// *`server`*/myPath/myImage.tif?req=imageprops`

Proprietà catalogo immagini query:

` http:// *`server`*/myRootId?req=catalogprops`

Accedi alle proprietà di una voce del catalogo immagini da JavaScript lato client incorporato in un file HTML:

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

Recupera l’immagine della maschera per una particolare voce di catalogo, ridimensionata al 25% delle dimensioni originali:

` http:// *`server`*/myRootId/myImageId?req=mask&scale=0.25`

Richiedi un&#39;immagine a una dimensione di un ottavo:

` http:// *`server`*/myRootId/myImageId?scl=8`

È lo stesso di:

` http:// *`server`*/myRootId/myImageId?req=img&scl=8`

Richiedi una miniatura di un’immagine, in base agli attributi di miniatura specificati nel catalogo immagini:

` http:// *`server`*/myRootId/myImageId?req=tmb&wid=64&hei=64`

Invia un SMS ai registri del server:

` http:// *`server`*/myRootId?req=message&message=This%20is%20the%20message`

## Consultate anche {#section-80cb0892c9174681b640985a1a26e590}

[fmt=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [catalogo::destinazioni](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalogo::DatiUtente](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md), [Ridimensionamento miniature](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f), [Proprietà](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9), [Mappe immagine](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)
