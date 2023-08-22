---
title: op_growMaskR
description: Dilatare/erodere l'immagine. Applica un dilatatore morfologico (raggio > 0) o un'erosione (raggio < 0) ai dati della maschera.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7abfbccf-8bcf-44d4-b50a-eca7a3f11360
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# op_growMaskR{#op-growmaskr}

Dilatare/erodere l&#39;immagine. Applica un dilatatore morfologico (raggio > 0) o un&#39;erosione (raggio &lt; 0) ai dati della maschera.

`op_growMaskR= *`raggioR`*`

<table id="simpletable_3BAA4523D29E447FA7A4C9009B3E8344"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> raggioR</span></span> </p> </td> 
  <td class="stentry"> <p>Dilatare/erodere il raggio in pixel dove <span class="codeph"><span class="varname"> raggioR</span></span> viene applicato così come è, indipendentemente dal fatto che la maschera venga ricampionata verso il basso (int -100..100). </p></td> 
 </tr> 
</table>

Utilizzato principalmente per ingrandire o ridurre leggermente una maschera per evitare artefatti lungo il bordo della maschera.

## Proprietà {#section-b1c66d65168d4ea695e8662ea690bd4e}

Si applica al livello corrente o al livello `0` se `layer=comp`.

## Predefinito {#section-14c908bb87cb42acbea709effea2f964}

`op_growMaskR=0`, senza alcuna modifica.

## Consultate anche {#section-ad3e5cecfc3448a38ea06093e015c88a}

[Effetti livello](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-layer-effects.md#reference-82a6b5311b3d4471ad2799adb3b2201c)

[op_grow](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a)

[op_growMask](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-growmask.md#reference-f0f9000af3ae43aba73d3ac1826710a1)
