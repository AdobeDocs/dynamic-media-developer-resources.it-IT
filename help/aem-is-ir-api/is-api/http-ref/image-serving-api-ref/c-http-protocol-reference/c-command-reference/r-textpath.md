---
description: Percorso del testo. Specifica il percorso da utilizzare come linea di base per il testo fornito con textPs=.
solution: Experience Manager
title: textPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---


# textPath{#textpath}

Percorso del testo. Specifica il percorso da utilizzare come linea di base per il testo fornito con textPs=.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Dati del percorso. </p></td> 
 </tr> 
</table>

Per ulteriori informazioni, inclusa una descrizione di *`pathDefinition`*, consulta [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) .

>[!NOTE]
>
>A differenza di `clipPath=`, i percorsi di testo non vengono chiusi automaticamente quando &quot;z&quot; o &quot;Z&quot; non è specificato alla fine di un sottopercorso.

*`pathDefinition`* possono includere più percorsi secondari. Il testo viene rappresentato sui percorsi secondari nell’ordine specificato.

I comandi RTF `\ql`, `\qc`, `\qr`, `\li` e `\ri` possono essere utilizzati per posizionare il testo sottoposto a rendering lungo il percorso.

## Proprietà {#section-068137df436c46b9b55d271eb60e7285}

Attributo del livello di testo ( solo `textPs=`). Ignorato da altri livelli. Si applica a `layer=0` se specificato per `layer=comp`. Ignorato se sono presenti `textPs=`.

Se un livello include sia `textPath=` che `textFlowPath=`, viene restituito un errore.

## Predefinito {#section-697b1f2cfc43498080a31327e6eb173d}

Nessuno, per il rendering di testo standard.

## Consultate anche {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), livelli  [di testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
