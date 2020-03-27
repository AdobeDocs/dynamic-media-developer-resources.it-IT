---
description: Area di esclusione del flusso di testo. Specifica una o più aree da escludere dal flusso di testo.
seo-description: Area di esclusione del flusso di testo. Specifica una o più aree da escludere dal flusso di testo.
seo-title: textFlowXPath
solution: Experience Manager
title: textFlowXPath
topic: Scene7 Image Serving - Image Rendering API
uuid: ce833ae7-e774-4954-a521-b6247e75f6eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# textFlowXPath{#textflowxpath}

Area di esclusione del flusso di testo. Specifica una o più aree da escludere dal flusso di testo.

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Dati percorso. </p></td> 
 </tr> 
</table>

Per ulteriori informazioni, inclusa una descrizione di [, vedere](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) clipPath= *`pathDefinition`*. Se non viene specificata alcuna definizione di percorso, `textFlowXPath=` viene ignorata.

## Proprietà {#section-cd1ebb151d4a405fbfc508d46522d686}

Attributo del livello di testo ( `textPs=` solo). Ignorato da altri livelli o se specificato senza `textFlowPath=`. Si applica a `layer=0` se specificato per `layer=comp`.

## Predefinito {#section-9405cda904684d829ed12a9e40a4dc46}

Nessuno.

## Consultate anche {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
