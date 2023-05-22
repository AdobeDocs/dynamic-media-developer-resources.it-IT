---
description: Larghezza visualizzazione. Specifica la larghezza dell’immagine di risposta (immagine di visualizzazione) quando fit= non è presente nella richiesta.
solution: Experience Manager
title: wid
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# wid{#wid}

Larghezza visualizzazione. Specifica la larghezza dell’immagine di risposta (immagine di visualizzazione) quando fit= non è presente nella richiesta.

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Larghezza immagine in pixel (int maggiore di 0). </p> </td> 
 </tr> 
</table>

Se entrambi `hei=` e `scl=` l&#39;immagine composita può essere ritagliata in base al `align=` attributo. Quando `fit=` è presente, `wid=` specifica la larghezza esatta, minima o massima dell’immagine di risposta; fai riferimento alla descrizione di `fit=` per i dettagli.

Se `scl=` non è specificato, l&#39;immagine composita viene ridimensionata per adattarla. Se entrambi `wid=` e `hei=` sono specificati, e `scl=` non è specificato, quindi l&#39;immagine viene ridimensionata per adattarsi completamente al rettangolo wid/hei, lasciando la minima area di sfondo esposta possibile. In questo caso, l&#39;immagine viene posizionata all&#39;interno del rettangolo di visualizzazione in base al `align=` attributo.

>[!NOTE]
>
>Viene restituito un errore se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`.

## Predefinito {#section-976d4c8554a34c899f85d172f6ac6f58}

Se nessuno dei due `wid=`, `hei=`, né `scl=` , l&#39;immagine di risposta avrà le dimensioni dell&#39;immagine composita oppure `attribute::DefaultPix`, a seconda di quale dei due valori è inferiore.

## Proprietà {#section-c93b7ce1b0d2475f80b06264b45d1285}

Visualizza attributo. Si applica indipendentemente dall&#39;impostazione del livello corrente.

## Esempio {#section-82bc98b7c15a451bbe9b915d414c0470}

Richiedi un&#39;immagine da inserire in un rettangolo 200x200; in alto a destra allinea l&#39;immagine se non è quadrata. Qualsiasi area di sfondo viene riempita con `attribute::BkgColor`.

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

La stessa immagine, distribuita a una larghezza fissa di 200 pixel, ma con altezza variabile per mantenere le proporzioni dell&#39;immagine. In questo caso, l&#39;immagine restituita non presenta mai aree di riempimento di sfondo. In questo caso align= non avrebbe alcun effetto.

` http:// *`server`*/myRootId/myImageId?wid=200`

## Consultate anche {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
