---
title: op_growMask
description: Dilatare/erodere l'immagine. Applica un dilatatore morfologico (raggio > 0) o un'erosione (raggio < 0) ai dati della maschera.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 322d97af-bb1b-44bb-90f1-cda9984b78b5
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# op_growMask{#op-growmask}

Dilatare/erodere l&#39;immagine. Applica un dilatatore morfologico (raggio > 0) o un&#39;erosione (raggio &lt; 0) ai dati della maschera.

`op_growMask= *`raggio`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> raggio</span> </p> </td> 
  <td class="stentry"> <p>Dilatare/erodere il raggio in pixel, dove si presume che venga applicato alla maschera a risoluzione completa e quindi viene ridotto per le maschere sottoposte a downsampling (int -100..100). </p></td> 
 </tr> 
</table>

Utilizzato principalmente per ingrandire o ridurre leggermente una maschera per evitare artefatti lungo il bordo della maschera.

## Proprietà {#section-b1c66d65168d4ea695e8662ea690bd4e}

Si applica al livello corrente o al livello `0` se `layer=comp`.

## Predefinito {#section-14c908bb87cb42acbea709effea2f964}

`op_growMask=0`, senza alcuna modifica.

## Consultate anche {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Effetti livello](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMaskR](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmaskr.md#reference-8092864159ae43c490821b9590d7709a)
