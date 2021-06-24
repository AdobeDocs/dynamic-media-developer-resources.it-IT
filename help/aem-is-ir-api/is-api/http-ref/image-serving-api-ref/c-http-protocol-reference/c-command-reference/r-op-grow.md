---
description: Dilata/erode immagine. Applica un dilato morfologico (raggio > 0) o un'erode (raggio < 0) ai dati dell'immagine.
solution: Experience Manager
title: op_grow
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---

# op_grow{#op-grow}

Dilata/erode immagine. Applica un dilato morfologico (raggio > 0) o un&#39;erode (raggio &lt; 0) ai dati dell&#39;immagine.

`op_grow= *`raggio`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> raggio</span></span> </p> </td> 
  <td class="stentry"> <p>Dilata/raggio di erosione in pixel (int -100.100). </p></td> 
 </tr> 
</table>

`*``*` radiosi in pixel rispetto all&#39;immagine composita. Se l’immagine è a colori, ogni componente viene elaborato in modo indipendente.

Utilizzato principalmente per modificare le dimensioni degli effetti di livello. È utile anche per ottenere effetti speciali sui livelli di testo o sui livelli a colori solidi con maschere.

## Proprietà {#section-b1c66d65168d4ea695e8662ea690bd4e}

Attributo livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`.

## Predefinito {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, senza modifiche.

## Consultate anche {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Effetti livello](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
