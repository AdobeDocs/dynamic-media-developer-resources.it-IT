---
title: printRes
description: Risoluzione di stampa. Sostituisce il valore della risoluzione di stampa incorporato nell'immagine di risposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# printRes{#printres}

Risoluzione di stampa. Sostituisce il valore della risoluzione di stampa incorporato nell&#39;immagine di risposta.

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Valore <span class="varname"></span> </p> </td> 
  <td class="stentry"> <p>Risoluzione di stampa (dpi). </p></td> 
 </tr> 
</table>

La risoluzione di stampa è normalmente definita da `catalog::PrintResolution` se si tratta di una voce di catalogo, altrimenti dal valore di risoluzione di stampa incorporato nell&#39;immagine di origine. Se è presente un modello o un&#39;immagine composita a livelli, la risoluzione di stampa predefinita incorporata nel file di risposta è la risoluzione di stampa dell&#39;immagine di livello con il numero di livello più basso.

L&#39;impostazione della risoluzione di stampa non modifica le dimensioni in pixel dell&#39;immagine di risposta.

## Proprietà {#section-03c7910ebe234804a319e5d0d8ef3a74}

Attributo della richiesta. Viene applicato indipendentemente dall&#39;impostazione del livello corrente.

## Predefinito {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution`
Oppure la risoluzione di stampa incorporata nell&#39;immagine sorgente.

## Consultate anche {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalogo::RisoluzioneStampa](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
