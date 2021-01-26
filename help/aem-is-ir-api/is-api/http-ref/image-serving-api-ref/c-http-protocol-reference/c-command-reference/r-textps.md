---
description: Testo livello ( compatibile con Adobe Photoshop). Specifica il corpo del testo per un livello di testo.
seo-description: Testo livello ( compatibile con Adobe Photoshop). Specifica il corpo del testo per un livello di testo.
seo-title: textPs
solution: Experience Manager
title: textPs
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 45e587b6-8dc8-408c-ade6-d70025fd1117
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 3%

---


# textPs{#textps}

Testo livello ( compatibile con Adobe Photoshop). Specifica il corpo del testo per un livello di testo.

`textPs= *`string`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> string</span> </span> </p> </td> 
  <td class="stentry"> <p>Stringa RTF (Rich Text Format). </p></td> 
 </tr> 
</table>

Tutti i controlli di formattazione di font, colore e paragrafo vengono eseguiti utilizzando i comandi RTF.

Vedere [Formattazione testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`textPs=` supporta funzioni estese, quali giustificazione, scorrimento del testo in aree non rettangolari definite con  `textFlowPath=` e/o  `textFlowXPath=`e rendering del testo lungo percorsi arbitrari definiti con  `textPath=`.

## Proprietà {#section-a289dc26b6534b41998b1e241d5f2f92}

Attributo layer. Si applica a `layer=0` se `layer=comp`. Esclusiva reciproca con `src=` e `text=` nello stesso livello. L&#39;ultima occorrenza di `text=`, `textPs=` e `src=` prevale e determina se si tratta di un&#39;immagine o di un livello di testo. Ignorato dai livelli degli effetti.

## Predefinito {#section-11c2ae2c96d64a0a9c207252df663e4d}

Nessuno.

## Consultate anche {#section-5c2b25767d2b47b5be817271ab12e13c}

[Formattazione](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) del testo,  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)  [textFlowXPath=, testoPath=, testoTestoAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
