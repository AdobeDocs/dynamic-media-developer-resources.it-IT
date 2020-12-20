---
description: Rettangolo di visualizzazione finale. Consente di smontare l'immagine di visualizzazione finale in più strisce o piastrelle, che possono essere distribuite separatamente e riassemblate dal cliente senza problemi, senza artefatti lungo i bordi.
seo-description: Rettangolo di visualizzazione finale. Consente di smontare l'immagine di visualizzazione finale in più strisce o piastrelle, che possono essere distribuite separatamente e riassemblate dal cliente senza problemi, senza artefatti lungo i bordi.
seo-title: rect
solution: Experience Manager
title: rect
topic: Scene7 Image Serving - Image Rendering API
uuid: c4830fc5-d102-4789-8753-0a660d4a557e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# rect{#rect}

Rettangolo di visualizzazione finale. Consente di smontare l&#39;immagine di visualizzazione finale in più strisce o piastrelle, che possono essere distribuite separatamente e riassemblate dal cliente senza problemi, senza artefatti lungo i bordi.

`rect= *``*, *``*[, *`coordsizescale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> accordo</span> </p> </td> 
  <td class="stentry"> <p>L'offset dei pixel dall'angolo superiore sinistro dell'immagine di visualizzazione all'angolo superiore sinistro del rettangolo di visualizzazione (int, int), espresso in pixel, dopo l'applicazione della scala <span class="varname"></span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> size</span> </p></td> 
  <td class="stentry"> <p>Dimensione del ROI in pixel (int, int). Specifica la dimensione dell'immagine della risposta. L'immagine viene riempita con <span class="codeph"> bgc=</span> nelle aree non coperte dall'immagine di visualizzazione (o lasciata trasparente, se nella richiesta è presente <span class="codeph"> fmt=*-alpha</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>Fattore di scala (reale). Valori inferiori a 1,0 riducono la risoluzione e valori maggiori di 1,0 aumentano la risoluzione. </p></td> 
 </tr> 
</table>

Con questo comando, Image Server può distribuire immagini di grandi dimensioni via HTTP che altrimenti supererebbero il limite configurato con `attribute::MaxPix`.

>[!NOTE]
>
>Per risultati ottimali con la compressione JPEG, la dimensione della striscia o della sezione deve essere un multiplo della dimensione della sezione di codifica JPEG (16x16 pixel).

## Esempio {#section-932fcfcb41d74a29bc929e4430c49601}

Separate un’immagine CMYK stampabile in diverse strisce a risoluzione piena per ridurre le dimensioni dei file da scaricare. Se dovessimo richiedere un&#39;immagine contigua:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

Innanzitutto, vengono ottenute informazioni pertinenti sull’immagine:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

La risposta testuale include le seguenti proprietà:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

In base a queste informazioni, decidiamo di volere quattro strisce da 600x2000 pixel. Il comando `rect=` viene utilizzato per descrivere le dimensioni e le posizioni della striscia.

Poiché l&#39;immagine viene modificata frequentemente, verrà incluso il comando `id=` per ridurre al minimo la possibilità di ottenere una o più strisce da una versione precedente dell&#39;immagine che potrebbe essere stata memorizzata nella cache in un server CDN o proxy. A questo scopo viene utilizzato il valore della proprietà `image.version`.

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Proprietà {#section-aae223cee13e46d38b74680c048d945b}

Visualizza attributo. Si applica indipendentemente dall’impostazione del livello corrente.

Tutte le aree del ROI che si estendono al di fuori dell&#39;immagine di visualizzazione vengono aggiunte con `bgc=`.

`rect=` importante viene applicato *dopo* il ridimensionamento finale e l&#39;adattamento con `scl=`, `wid=`, `hei=`, `fit=`, `rgn=` e `align=`.

## Predefinito {#section-b296d3bbfb19441f87137a452b70f19a}

Immagine di visualizzazione completa e non modificata ( `rect=0,0,width,height,1.0`).

## Vedere anche {#section-74015202c0c545ec82aec614d74b4bbd}

[ritaglio=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [estendi=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f)  [ ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)  [align=, fit=attributo::MaxPix, id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
