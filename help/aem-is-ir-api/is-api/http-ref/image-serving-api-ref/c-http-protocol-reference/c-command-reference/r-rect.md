---
description: Rettangolo della vista finale. Consente di smontare l'immagine finale in diverse strisce o tessere, che possono essere consegnate separatamente e riassemblate dal cliente senza interruzioni, senza artefatti lungo i bordi.
solution: Experience Manager
title: retto
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1870001b-7904-470f-9582-984d453509ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 0%

---

# retto{#rect}

Rettangolo della vista finale. Consente di smontare l&#39;immagine finale in diverse strisce o tessere, che possono essere consegnate separatamente e riassemblate dal cliente senza interruzioni, senza artefatti lungo i bordi.

`rect= *`corda`*, *`dimensione`*[, *`scala`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> corda</span> </p> </td> 
  <td class="stentry"> <p>Offset pixel dall'angolo superiore sinistro dell'immagine di visualizzazione all'angolo superiore sinistro del rettangolo di visualizzazione (int, int), espresso in pixel, dopo <span class="varname"> scala</span> viene applicata. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> dimensione</span> </p></td> 
  <td class="stentry"> <p>Dimensione del ROI in pixel (int, int). Specifica la dimensione dell'immagine di risposta. L'immagine è piena di <span class="codeph"> bgc=</span> nelle aree non coperte dall'immagine di visualizzazione (o non trasparenti se <span class="codeph"> fmt=*-alpha</span> è presente nella richiesta). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>Fattore di scala (reale). I valori inferiori a 1,0 riducono la risoluzione e i valori superiori a 1,0 aumentano la risoluzione. </p></td> 
 </tr> 
</table>

Utilizzando questo comando, Image Server può distribuire immagini di grandi dimensioni tramite HTTP che altrimenti supererebbero il limite configurato con `attribute::MaxPix`.

>[!NOTE]
>
>Per risultati ottimali quando si utilizza la compressione JPEG, la dimensione della striscia o del riquadro deve essere un multiplo della dimensione del riquadro di codifica JPEG (16x16 pixel).

## Esempio {#section-932fcfcb41d74a29bc929e4430c49601}

Separare un&#39;immagine CMYK stampabile in diverse strisce a risoluzione completa per ridurre le dimensioni dei file di download. Se richiedessimo un’immagine contigua:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

In primo luogo, si ottengono informazioni rilevanti sull&#39;immagine:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

La risposta testuale include le seguenti proprietà:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

In base a queste informazioni, decidiamo di volere quattro strisce pixel da 600x2000. Il `rect=` Il comando viene utilizzato per descrivere le dimensioni e le posizioni delle strisce.

Poiché questa immagine viene modificata frequentemente, includeremo `id=` comando per ridurre al minimo la possibilità di avere una o più strisce di una versione precedente dell’immagine memorizzate nella cache in una rete CDN o in un server proxy. Il valore della proprietà `image.version` viene utilizzata a questo scopo.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Proprietà {#section-aae223cee13e46d38b74680c048d945b}

Visualizza attributo. Si applica indipendentemente dall&#39;impostazione del livello corrente.

Tutte le aree del ROI che si estendono all&#39;esterno dell&#39;immagine di visualizzazione vengono imbottite con `bgc=`.

Importante `rect=` viene applicato *dopo* ridimensionamento e adattamento finale con `scl=`, `wid=`, `hei=`, `fit=`, `rgn=`, e `align=`.

## Predefinito {#section-b296d3bbfb19441f87137a452b70f19a}

Immagine vista intera e non modificata ( `rect=0,0,width,height,1.0`).

## Vedi anche {#section-74015202c0c545ec82aec614d74b4bbd}

[crop= ritaglio](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extend= estensione](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rgn=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5), [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
