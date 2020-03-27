---
description: Dilata/erode immagine. Applica ai dati della maschera un dilato morfologico (raggio > 0) o un'erode (raggio < 0).
seo-description: Dilata/erode immagine. Applica ai dati della maschera un dilato morfologico (raggio > 0) o un'erode (raggio < 0).
seo-title: op_developMaskR
solution: Experience Manager
title: op_developMaskR
topic: Scene7 Image Serving - Image Rendering API
uuid: b81968e7-ebaf-426c-9230-1afcf4b5cf24
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_developMaskR{#op-growmaskr}

Dilata/erode immagine. Applica ai dati della maschera un dilato morfologico (raggio > 0) o un&#39;erode (raggio &lt; 0).

`op_growMaskR= *`radiusR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radiusR</span></span> </p> </td> 
  <td class="stentry"> <p>Dilatare/ridurre il raggio in pixel in cui viene applicato il <span class="codeph"><span class="varname"> raggioR</span></span> , indipendentemente dal fatto che la maschera sia sottoposta a downsampling (int -100.100). </p></td> 
 </tr> 
</table>

Utilizzata principalmente per ingrandire o ridurre leggermente una maschera per evitare artefatti intorno al bordo della maschera.

## Proprietà {#section-b1c66d65168d4ea695e8662ea690bd4e}

Si applica al livello corrente o al livello `0` se `layer=comp`.

## Predefinito {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, senza modifiche.

## Consultate anche {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Effetti livello](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_develop](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_developMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
