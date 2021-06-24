---
description: Altezza visualizzazione. Specifica l'altezza dell'immagine della risposta (visualizza immagine) quando l'adattamento non è presente nella richiesta.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 3%

---

# hei{#hei}

Altezza visualizzazione. Specifica l&#39;altezza dell&#39;immagine della risposta (visualizza immagine) quando l&#39;adattamento non è presente nella richiesta.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Altezza immagine in pixel (in numero maggiore di 0). </p> </td> 
 </tr> 
</table>

Se sono specificati sia `wid=` che `scl=`, l&#39;immagine composita può essere ritagliata in base all&#39;attributo `align=`. Quando `fit=` è presente, `hei=` specifica l&#39;esatta, la minima o l&#39;altezza massima dell&#39;immagine di risposta; per ulteriori informazioni, fare riferimento alla descrizione di ` [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)` .

Se `scl=` non è specificato, l&#39;immagine composita viene ridimensionata per adattarsi. Se sono specificati sia `wid=` che `hei=` e `scl=` non è specificato, l&#39;immagine viene ridimensionata in modo da adattarsi interamente al rettangolo wid/hei, lasciando il minor spazio di sfondo possibile esposto; in questo caso, l&#39;immagine viene posizionata all&#39;interno del rettangolo di visualizzazione secondo l&#39;attributo `align=` . L&#39;area di sfondo viene riempita con `bgc=`, oppure, se non specificato con `attribute::BkgColor`.

>[!NOTE]
>
>Se la dimensione dell&#39;immagine di risposta calcolata è maggiore di `attribute::MaxPix`, viene restituito un errore.

## Proprietà {#section-534923644a1e464496eeba83dedcbd3c}

Visualizza attributo. Si applica indipendentemente dall&#39;impostazione del livello corrente.

## Predefinito {#section-76544d34806d4124a8b173e229cba71f}

Se non vengono specificati né `wid=`, `hei=`, né `scl=`, l&#39;immagine di risposta ha le dimensioni dell&#39;immagine composita o `attribute::DefaultPix`, a seconda di quale sia la dimensione minore.

## Esempi {#section-eb10df7cd67e4733984810aaffd0b9e2}

Richiedere un&#39;immagine per inserirla in un rettangolo 200x200; allineate l&#39;immagine in alto a sinistra se non è quadrata. Ogni area di sfondo viene riempita con `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

La stessa immagine, distribuita ad un&#39;altezza fissa di 200 pixel, ma con una larghezza variabile per corrispondere alle proporzioni dell&#39;immagine. In questo caso, l&#39;immagine restituita non ha mai aree di riempimento di sfondo. In questo caso `align=` non avrebbe alcun effetto.

`http://server/myRootId/myImageId?hei=200`

## Consultate anche {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [rng=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f),  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
