---
description: Rettangolo di visualizzazione finale. Consente di smontare l'immagine della vista finale in più strisce o piastrelle, che possono essere consegnate separatamente e riassemblate dal cliente senza problemi, senza artefatti lungo i bordi.
solution: Experience Manager
title: rect
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 1%

---


# rect{#rect}

Rettangolo di visualizzazione finale. Consente di smontare l&#39;immagine della vista finale in più strisce o piastrelle, che possono essere consegnate separatamente e riassemblate dal cliente senza problemi, senza artefatti lungo i bordi.

`rect= *``*, *``*[, *`coordsizescale`*]`

<table id="simpletable_69D112F85FA24EFCA727B398DC8ED699"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> corda</span> </p> </td> 
  <td class="stentry"> <p>Offset pixel dall'angolo in alto a sinistra dell'immagine di visualizzazione all'angolo in alto a sinistra del rettangolo di visualizzazione (int, int), espresso in pixel, dopo l'applicazione della <span class="varname"> scala</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> size</span> </p></td> 
  <td class="stentry"> <p>Dimensione del ROI in pixel (int, int). Specifica la dimensione dell'immagine di risposta. L'immagine viene riempita con <span class="codeph"> bgc=</span> in aree non coperte dall'immagine di visualizzazione (o lasciata trasparente, se <span class="codeph"> fmt=*-alpha</span> è presente nella richiesta). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> scale</span> </p></td> 
  <td class="stentry"> <p>Fattore di scala (reale). Valori inferiori a 1,0 riducono la risoluzione e valori superiori a 1,0 aumentano la risoluzione. </p></td> 
 </tr> 
</table>

Utilizzando questo comando, Image Server può fornire immagini di grandi dimensioni tramite HTTP che altrimenti supererebbero il limite di dimensione configurato con `attribute::MaxPix`.

>[!NOTE]
>
>Per ottenere risultati ottimali con la compressione JPEG, la dimensione della striscia o del riquadro deve essere un multiplo della dimensione del riquadro di codifica JPEG (16x16 pixel).

## Esempio {#section-932fcfcb41d74a29bc929e4430c49601}

Separa un&#39;immagine CMYK stampabile in diverse strisce a risoluzione piena per ridurre le dimensioni del file da scaricare. Se dovessimo richiedere un&#39;immagine contigua:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&fmt=tif&icc=WebCoated`

In primo luogo, si ottengono informazioni rilevanti sull&#39;immagine:

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&req=props`

La risposta testuale include le seguenti proprietà:

`image.width=2000 image.height=2400 image.version=37JK6NTvpvC42F5gOuLEVY`

In base a queste informazioni, decidiamo di volere quattro strisce di pixel 600x2000. Il comando `rect=` viene utilizzato per descrivere le dimensioni e le posizioni della striscia.

Poiché questa immagine viene cambiata frequentemente, includeremo il comando `id=` per ridurre al minimo la possibilità di finire con una o più strisce di una versione precedente dell&#39;immagine che potrebbero essere state memorizzate nella cache in un CDN o in un server proxy. A questo scopo viene utilizzato il valore della proprietà `image.version` .

`http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,0,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,600,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1200,2000,600 http://server/is/image/cat/imageId?scl=1&op_usm=.9,2&bgc=ffffff&id=37JK6NTvpvC42F5gOuLEVY&rect=0,1800,2000,600`

## Proprietà {#section-aae223cee13e46d38b74680c048d945b}

Visualizza attributo. Si applica indipendentemente dall&#39;impostazione del livello corrente.

Tutte le aree del ROI che si estendono al di fuori dell&#39;immagine visualizzata vengono aggiunte con `bgc=`.

`rect=` importante viene applicato *dopo* il ridimensionamento e il montaggio finali con `scl=`, `wid=`, `hei=`, `fit=`, `rgn=` e `align=`.

## Predefinito {#section-b296d3bbfb19441f87137a452b70f19a}

Immagine di visualizzazione completa e non modificata ( `rect=0,0,width,height,1.0`).

## Vedere Anche {#section-74015202c0c545ec82aec614d74b4bbd}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [rng=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rgn.md#reference-daa9b80e0d8c4b1aa67d116b578d592f),  [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5),  [id=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0)
