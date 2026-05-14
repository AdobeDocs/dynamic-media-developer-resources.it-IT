---
title: op_grow
description: Dilatare/erodere l'immagine. Applica un dilatatore morfologico (raggio > 0) o un'erosione (raggio < 0) ai dati dell'immagine.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4c5bef4e-f80e-454d-8e93-30bf33d7ec9e
TQID: 'https://experienceleague.adobe.com/vNFqqzcSqktgB5ohUZjqf0RtQNOD-t7fxITR2gZl-T4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 2%

---

# op_grow{#op-grow}

Dilatare/erodere l&#39;immagine. Applica un dilatatore morfologico (raggio > 0) o un&#39;erosione (raggio &lt; 0) ai dati dell&#39;immagine.

`op_grow= *`raggio`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Raggio <span class="codeph"><span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>Dilata/erode raggio in pixel (int -100..100). </p></td> 
 </tr> 
</table>

`*`raggio`*` è espresso in pixel rispetto all&#39;immagine composita. Se l&#39;immagine è a colori, ogni componente viene elaborato in modo indipendente.

Utilizzato principalmente per modificare le dimensioni degli effetti di livello. Utile anche per ottenere effetti speciali sui livelli testo o sui livelli colore a tinta unita con maschere.

## Proprietà {#section-b1c66d65168d4ea695e8662ea690bd4e}

Attributo livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`.

## Predefinito {#section-14c908bb87cb42acbea709effea2f964}

`op_grow=0`, senza modifiche.

## Consultate anche {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Effetti livello](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)
