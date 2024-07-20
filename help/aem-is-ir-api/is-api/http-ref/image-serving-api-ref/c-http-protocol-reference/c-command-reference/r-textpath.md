---
title: textPath
description: Percorso testo. Specifica il percorso da utilizzare come linea di base per il testo fornito con textPs=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---

# textPath{#textpath}

Percorso testo. Specifica il percorso da utilizzare come linea di base per il testo fornito con textPs=.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Dati percorso. </p></td> 
 </tr> 
</table>

Per ulteriori informazioni, inclusa una descrizione di *`pathDefinition`*, vedere [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d).

>[!NOTE]
>
>A differenza di `clipPath=`, i percorsi di testo non vengono chiusi automaticamente quando &#39;z&#39; o &#39;Z&#39; non è specificato alla fine di un percorso secondario.

*`pathDefinition`* può includere più percorsi secondari. Il rendering del testo viene eseguito sui percorsi secondari nell&#39;ordine specificato.

I comandi RTF `\ql`, `\qc`, `\qr`, `\li` e `\ri` possono essere utilizzati per posizionare il testo sottoposto a rendering lungo il percorso.

## Proprietà {#section-068137df436c46b9b55d271eb60e7285}

Attributo livello testo (solo `textPs=`). Ignorato da altri livelli. Si applica a `layer=0` se specificato per `layer=comp`. Ignorato se `textPs=` sono presenti.

Se un livello include sia `textPath=` che `textFlowPath=`, viene restituito un errore.

## Predefinito {#section-697b1f2cfc43498080a31327e6eb173d}

Nessuno, per il rendering di testo standard.

## Consultate anche {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [Livelli di testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
