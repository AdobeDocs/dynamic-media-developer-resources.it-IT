---
title: hei
description: Altezza visualizzazione. Specifica l’altezza dell’immagine di risposta (immagine di visualizzazione) quando fit non è presente nella richiesta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c812c7f0-4ac1-42cb-be47-7baebd8caf60
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---

# hei{#hei}

Altezza visualizzazione. Specifica l’altezza dell’immagine di risposta (immagine di visualizzazione) quando fit non è presente nella richiesta.

` hei= *`val`*`

<table id="simpletable_1A36827B6E6647888A4E6E868975D716"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Altezza immagine in pixel (int maggiore di 0). </p> </td> 
 </tr> 
</table>

Se sono specificati sia `wid=` che `scl=`, l&#39;immagine composita potrebbe essere ritagliata in base all&#39;attributo `align=`. Quando `fit=` è presente, `hei=` specifica l&#39;altezza esatta, minima o massima dell&#39;immagine di risposta. Per ulteriori informazioni, fare riferimento alla descrizione di [fit=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md).

Se `scl=` non è specificato, l&#39;immagine composita viene ridimensionata per adattarla. Se sono specificati sia `wid=` che `hei=` e `scl=` non è specificato, l&#39;immagine viene ridimensionata per rientrare completamente nel rettangolo wid/hei, lasciando il minor numero possibile di aree di sfondo esposte. In questo caso, l&#39;immagine viene posizionata all&#39;interno del rettangolo di visualizzazione in base all&#39;attributo `align=`. L&#39;area di sfondo è riempita con `bgc=` o, se non specificato, con `attribute::BkgColor`.

>[!NOTE]
>
>Viene restituito un errore se le dimensioni dell&#39;immagine di risposta calcolate sono maggiori di `attribute::MaxPix`.

## Proprietà {#section-534923644a1e464496eeba83dedcbd3c}

Visualizza attributo. Viene applicato indipendentemente dall&#39;impostazione del livello corrente.

## Predefinito {#section-76544d34806d4124a8b173e229cba71f}

Se non vengono specificati né `wid=`, `hei=`, né `scl=`, le dimensioni dell&#39;immagine di risposta corrispondono a quelle dell&#39;immagine composita oppure a `attribute::DefaultPix`, a seconda di quale dei due valori è minore.

## Esempi {#section-eb10df7cd67e4733984810aaffd0b9e2}

Richiedi un&#39;immagine in modo che possa rientrare in un rettangolo di 200x200; in alto a sinistra allinea l&#39;immagine se non è quadrata. Qualsiasi area di sfondo è riempita con `attribute::BkgColor`.

`http://server/myRootId/myImageId?wid=200&hei=200&align=-1,-1`

La stessa immagine, distribuita a un&#39;altezza fissa di 200 pixel, ma con una larghezza variabile che corrisponde alle proporzioni dell&#39;immagine. In questo caso, l&#39;immagine restituita non presenta mai aree di riempimento di sfondo. E in questo caso `align=` non avrebbe alcun effetto.

`http://server/myRootId/myImageId?hei=200`

## Consultate anche {#section-796e059e42ea4e86ab90ea3d024850ec}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
