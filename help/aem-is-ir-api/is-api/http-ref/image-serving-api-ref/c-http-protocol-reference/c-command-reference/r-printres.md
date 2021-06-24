---
description: Risoluzione di stampa. Sostituisce il valore della risoluzione di stampa incorporato nell'immagine di risposta.
solution: Experience Manager
title: printRes
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---

# printRes{#printres}

Risoluzione di stampa. Sostituisce il valore della risoluzione di stampa incorporato nell&#39;immagine di risposta.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Risoluzione di stampa (dpi). </p></td> 
 </tr> 
</table>

La risoluzione di stampa viene normalmente definita da `catalog::PrintResolution` in caso di voce di catalogo, altrimenti dal valore di risoluzione di stampa incorporato nell&#39;immagine sorgente. Nel caso di un modello o di un&#39;immagine composita a livelli, la risoluzione di stampa predefinita incorporata nel file di risposta è la risoluzione di stampa dell&#39;immagine di livello con il numero di livello più basso.

L&#39;impostazione della risoluzione di stampa non modifica la dimensione in pixel dell&#39;immagine di risposta.

## Proprietà {#section-03c7910ebe234804a319e5d0d8ef3a74}

Attributo di richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente.

## Predefinito {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` o la risoluzione di stampa incorporata nell&#39;immagine sorgente.

## Consultate anche {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalogo::PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
