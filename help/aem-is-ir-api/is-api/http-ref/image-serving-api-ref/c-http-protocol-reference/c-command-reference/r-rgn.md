---
title: rgn
description: Regione di interesse. Specifica una regione di interesse rettangolare (ROI) nell'immagine composita, espressa in pixel.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fa597ba-f949-47f2-bb0f-5c078b5c7524
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# rgn{#rgn}

Regione di interesse. Specifica una regione di interesse rettangolare (ROI) nell&#39;immagine composita, espressa in pixel.

rgn= *`coord`*, *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> corda</span> </p> </td> 
  <td class="stentry"> <p>Offset pixel dall'angolo superiore sinistro dell'immagine composita all'angolo superiore sinistro del ROI (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> dimensione</span> </p></td> 
  <td class="stentry"> <p>Dimensione del ROI in pixel (int, int). </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` definisce solo un ROI senza ritagliare l’immagine. Quando `wid=` e/o `hei=` vengono applicate anche dimensioni maggiori di, i dati aggiuntivi dell’immagine composita potrebbero essere visibili nell’immagine di risposta finale.

## Proprietà {#section-53edb35f4e364d7ca13fd0886e8b0c86}

Visualizza attributo. Si applica indipendentemente dall&#39;impostazione del livello corrente.

Tutte le aree del ROI che si estendono all&#39;esterno dell&#39;immagine composita sono imbottite con `bgc=`.

`rgn=` viene applicato prima della modifica in scala finale e dell&#39;adattamento con `scl=`, `wid=`, `hei=`, `fit=`, `rect=`, o `align=`.

## Predefinito {#section-6a3df8f670084def900ffef9dab7e94a}

Immagine composita intera ( `rgn=0,0,width,height`).

## Consultate anche {#section-07883760f25c4d17aedbee36b7883891}

[crop= ritaglio](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) , [extend= estensione](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47), [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
