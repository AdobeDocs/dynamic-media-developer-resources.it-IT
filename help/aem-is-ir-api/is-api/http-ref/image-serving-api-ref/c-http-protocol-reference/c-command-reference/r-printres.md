---
description: Risoluzione di stampa. Sostituisce il valore della risoluzione di stampa incorporato nell’immagine di risposta.
seo-description: Risoluzione di stampa. Sostituisce il valore della risoluzione di stampa incorporato nell’immagine di risposta.
seo-title: printRes
solution: Experience Manager
title: printRes
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a62611a-b3b9-4f20-834f-e34e75d33ddd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# printRes{#printres}

Risoluzione di stampa. Sostituisce il valore della risoluzione di stampa incorporato nell’immagine di risposta.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Risoluzione di stampa (dpi). </p></td> 
 </tr> 
</table>

La risoluzione di stampa è normalmente definita `catalog::PrintResolution` in caso di voce di catalogo, altrimenti viene utilizzata per il valore di risoluzione di stampa incorporato nell’immagine sorgente. Nel caso di un modello o di un’immagine composita a livelli, la risoluzione di stampa predefinita incorporata nel file di risposta corrisponde alla risoluzione di stampa dell’immagine del livello con il numero di livello più basso.

L&#39;impostazione della risoluzione di stampa non modifica la dimensione in pixel dell&#39;immagine di risposta.

## Proprietà {#section-03c7910ebe234804a319e5d0d8ef3a74}

Attributo di richiesta. Si applica indipendentemente dall’impostazione del livello corrente.

## Predefinito {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` o la risoluzione di stampa incorporata nell’immagine sorgente.

## Consultate anche {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalogo:PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
