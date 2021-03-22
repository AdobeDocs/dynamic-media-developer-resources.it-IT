---
description: Area di flusso del testo. Specifica una o più aree in cui deve essere eseguito lo scorrimento del testo specificato con textPs=.
seo-description: Area di flusso del testo. Specifica una o più aree in cui deve essere eseguito lo scorrimento del testo specificato con textPs=.
seo-title: textFlowPath
solution: Experience Manager
title: textFlowPath
uuid: 5449d78f-e56b-4afb-a05a-7cf8f1f37278
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---


# textFlowPath{#textflowpath}

Area di flusso del testo. Specifica una o più aree in cui deve essere eseguito lo scorrimento del testo specificato con textPs=.

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition  </span> </p> </td> 
  <td class="stentry"> <p>Dati del percorso. </p> </td> 
 </tr> 
</table>

Per ulteriori informazioni, inclusa una descrizione di *`pathDefinition`*, consulta [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) .

I comandi dei margini RTF `\margl`, `\margr`, `\margt` e `\margb` vengono ignorati quando è presente `textFlowPath=`. Se non viene specificata alcuna definizione del percorso, `textFlowPath=` viene ignorato.

## Proprietà {#section-b68dc887c6534ce8982cad740b3aeaa4}

Attributo del livello di testo ( solo `textPs=`). Ignorato da altri livelli. Si applica a `layer=0` se specificato per `layer=comp`.

## Predefinito {#section-68c4559b9e8242059b82e5a39a455dfc}

come il rettangolo di livello; il testo riempie l&#39;intero rettangolo del livello.

## Consultate anche {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15), livelli  [di testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
