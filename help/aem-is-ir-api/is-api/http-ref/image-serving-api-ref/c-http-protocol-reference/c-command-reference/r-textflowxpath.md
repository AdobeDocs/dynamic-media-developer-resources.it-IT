---
description: Area di esclusione del flusso di testo. Specifica una o più aree da escludere dal flusso di testo.
solution: Experience Manager
title: textFlowXPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 5%

---


# textFlowXPath{#textflowxpath}

Area di esclusione del flusso di testo. Specifica una o più aree da escludere dal flusso di testo.

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Dati del percorso. </p></td> 
 </tr> 
</table>

Per ulteriori informazioni, inclusa una descrizione di *`pathDefinition`*, consulta [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) . Se non viene specificata alcuna definizione del percorso, `textFlowXPath=` viene ignorato.

## Proprietà {#section-cd1ebb151d4a405fbfc508d46522d686}

Attributo del livello di testo ( solo `textPs=`). Ignorato da altri livelli o se specificato senza `textFlowPath=`. Si applica a `layer=0` se specificato per `layer=comp`.

## Predefinito {#section-9405cda904684d829ed12a9e40a4dc46}

Nessuno.

## Consultate anche {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
