---
description: Altezza visualizzazione. Specifica l'altezza dell'immagine della risposta (immagine di visualizzazione) quando l'adattamento non è presente nella richiesta.
seo-description: Altezza visualizzazione. Specifica l'altezza dell'immagine della risposta (immagine di visualizzazione) quando l'adattamento non è presente nella richiesta.
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 307952bb-604f-49b4-bce3-b7a7fc7ec63b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 4%

---


# hei{#hei}

Altezza visualizzazione. Specifica l&#39;altezza dell&#39;immagine della risposta (immagine di visualizzazione) quando l&#39;adattamento non è presente nella richiesta.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Altezza immagine in pixel (in numero maggiore di 0). </p> </td> 
 </tr> 
</table>

Se sono specificati sia `wid=` che `scl=`, l&#39;immagine composita può essere ritagliata in base all&#39;attributo `align=`. Se è presente `fit=`, `hei=` specifica l&#39;esatta, il minimo o l&#39;altezza massima dell&#39;immagine di risposta; fare riferimento alla descrizione di ` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)` per ulteriori dettagli.

Se `scl=` non è specificato, l&#39;immagine composita viene ridimensionata per adattarsi. Se sono specificati sia `wid=` che `hei=` e `scl=` non è specificato, l&#39;immagine viene ridimensionata in modo da rientrare interamente all&#39;interno del rettangolo wid/hei, lasciando esposto il minor numero possibile di area di sfondo; in questo caso, l&#39;immagine viene posizionata all&#39;interno del rettangolo di visualizzazione in base all&#39;attributo `align=`. L&#39;area di sfondo è riempita con `bgc=`, oppure, se non è specificata con `attribute::BkgColor`.

>[!NOTE]
>
>Se la dimensione dell&#39;immagine di risposta calcolata è maggiore di `attribute::MaxPix`, viene restituito un errore.

## Proprietà {#section-534923644a1e464496eeba83dedcbd3c}

Visualizza attributo. Si applica indipendentemente dall’impostazione del livello corrente.

## Predefinito {#section-76544d34806d4124a8b173e229cba71f}

Se non vengono specificati né `wid=`, `hei=`, né `scl=`, l&#39;immagine di risposta ha le dimensioni dell&#39;immagine composita oppure `attribute::DefaultPix`, se è più piccola.

## Esempi {#section-eb10df7cd67e4733984810aaffd0b9e2}

Richiedete un’immagine da inserire in un rettangolo da 200x200; in alto a sinistra allinea l’immagine se non è quadrata. Ogni area di sfondo viene riempita con `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

La stessa immagine, trasmessa a un’altezza fissa di 200 pixel, ma con una larghezza variabile che corrisponda alle proporzioni dell’immagine. In questo caso, l&#39;immagine restituita non ha mai aree di riempimento di sfondo. In questo caso `align=` non avrebbe alcun effetto.

`http://server/myRootId/myImageId?hei=200`

## Consultate anche {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)  [rGN=, attribute::DefaultPix, attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
