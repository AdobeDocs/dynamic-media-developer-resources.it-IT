---
description: Regione di interesse. Specifica una regione di interesse rettangolare (ROI) nell'immagine composita, espressa in pixel.
seo-description: Regione di interesse. Specifica una regione di interesse rettangolare (ROI) nell'immagine composita, espressa in pixel.
seo-title: rassegnare
solution: Experience Manager
title: rassegnare
uuid: 08657925-c52a-4279-8357-c26ad5c5ef3d
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# rng{#rgn}

Regione di interesse. Specifica una regione di interesse rettangolare (ROI) nell&#39;immagine composita, espressa in pixel.

rng= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> corda</span> </p> </td> 
  <td class="stentry"> <p>Offset pixel dall’angolo in alto a sinistra dell’immagine composita all’angolo in alto a sinistra del ROI (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> size</span> </p></td> 
  <td class="stentry"> <p>Dimensione del ROI in pixel (int, int). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` definisce solo un ROI senza ritagliare l&#39;immagine. Se si applicano anche le dimensioni `wid=` e/o `hei=` maggiori di quelle dell&#39;immagine composita, nell&#39;immagine di risposta finale potrebbero essere visibili dati aggiuntivi dell&#39;immagine composita.

## Proprietà {#section-53edb35f4e364d7ca13fd0886e8b0c86}

Visualizza attributo. Si applica indipendentemente dall&#39;impostazione del livello corrente.

Tutte le aree del ROI che si estendono al di fuori dell&#39;immagine composita vengono aggiunte con `bgc=`.

`rgn=` viene applicato prima della scala finale e del montaggio con  `scl=`,  `wid=`,  `hei=`,  `fit=`,  `rect=` o  `align=`.

## Predefinito {#section-6a3df8f670084def900ffef9dab7e94a}

Immagine composita intera ( `rgn=0,0,width,height`).

## Consultate anche {#section-07883760f25c4d17aedbee36b7883891}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ,  [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
