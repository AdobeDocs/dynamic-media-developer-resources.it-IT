---
title: textFlowPath
description: Area di testo. Specifica una o più aree in cui far scorrere il testo specificato con textPs=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b5575d17-150b-421c-b298-077b577eb95c
TQID: 'https://experienceleague.adobe.com/jh0UxfQzO3UY8nogOZl4f0qHSGGG-fUC7AKtEPdGvOs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 2%

---

# textFlowPath{#textflowpath}

Area di testo. Specifica una o più aree in cui far scorrere il testo specificato con textPs=.

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> definizione percorso </span> </p> </td> 
  <td class="stentry"> <p>Dati percorso. </p> </td> 
 </tr> 
</table>

Per ulteriori informazioni, inclusa una descrizione di *`pathDefinition`*, vedere [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d).

I comandi di margine RTF `\margl`, `\margr`, `\margt` e `\margb` vengono ignorati quando è presente `textFlowPath=`. Se non viene specificata alcuna definizione di percorso, `textFlowPath=` verrà ignorato.

## Proprietà {#section-b68dc887c6534ce8982cad740b3aeaa4}

Attributo livello testo (solo `textPs=`). Ignorato da altri livelli. Si applica a `layer=0` se specificato per `layer=comp`.

## Predefinito {#section-68c4559b9e8242059b82e5a39a455dfc}

Come il rettangolo del livello; il testo riempie l&#39;intero rettangolo del livello.

## Consultate anche {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15), [Livelli di testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
