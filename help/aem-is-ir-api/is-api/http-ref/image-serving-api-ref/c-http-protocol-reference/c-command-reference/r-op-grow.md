---
description: Dilata/erode immagine. Applica un dilato morfologico (raggio > 0) o un'eruzione (raggio < 0) ai dati dell'immagine.
seo-description: Dilata/erode immagine. Applica un dilato morfologico (raggio > 0) o un'eruzione (raggio < 0) ai dati dell'immagine.
seo-title: op_develop
solution: Experience Manager
title: op_develop
topic: Scene7 Image Serving - Image Rendering API
uuid: bc9bf889-f7e1-4a65-b6d6-7e1257ef8c11
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# op_develop{#op-grow}

Dilata/erode immagine. Applica un dilato morfologico (raggio > 0) o un&#39;eruzione (raggio &lt; 0) ai dati dell&#39;immagine.

`op_grow= *`radius`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> radius</span></span> </p> </td> 
  <td class="stentry"> <p>Dilata/Raggio in pixel (numero intero -100.100). </p></td> 
 </tr> 
</table>

` *``*` radiosi in pixel rispetto all’immagine composita. Se l’immagine è a colori, ogni componente viene elaborato in modo indipendente.

Utilizzata principalmente per modificare le dimensioni degli effetti livello. È utile anche per ottenere effetti speciali sui livelli di testo o di colore in tinta unita con maschere.

## Proprietà {#section-b1c66d65168d4ea695e8662ea690bd4e}

Attributo layer. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`.

## Predefinito {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, senza modifiche.

## Consultate anche {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Effetti livello](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
