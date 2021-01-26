---
description: Percorso del testo. Specifica il percorso da utilizzare come linea di base per il testo fornito con textPs=.
seo-description: Percorso del testo. Specifica il percorso da utilizzare come linea di base per il testo fornito con textPs=.
seo-title: textPath
solution: Experience Manager
title: textPath
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a2f0047b-ad62-4605-a723-b43d53fbea56
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---


# textPath{#textpath}

Percorso del testo. Specifica il percorso da utilizzare come linea di base per il testo fornito con textPs=.

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
>A differenza di `clipPath=`, i percorsi di testo non vengono chiusi automaticamente quando &#39;z&#39; o &#39;Z&#39; non è specificato alla fine di un sottotracciato.

*`pathDefinition`* possono includere più sottopercorsi. Il testo viene rappresentato sui sottotracciati nell’ordine specificato.

I comandi RTF `\ql`, `\qc`, `\qr`, `\li` e `\ri` possono essere utilizzati per posizionare il testo rappresentato lungo il percorso.

## Proprietà {#section-068137df436c46b9b55d271eb60e7285}

Attributo del livello di testo ( solo `textPs=`). Ignorato da altri livelli. Si applica a `layer=0` se specificato per `layer=comp`. Ignorato se sono presenti `textPs=`.

Se un livello include sia `textPath=` che `textFlowPath=`, viene restituito un errore.

## Predefinito {#section-697b1f2cfc43498080a31327e6eb173d}

Nessuno, per il rendering di testo standard.

## Consultate anche {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), livelli di  [testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
