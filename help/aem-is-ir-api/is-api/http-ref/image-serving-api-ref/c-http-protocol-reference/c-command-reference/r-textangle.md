---
description: Direzione rendering testo. Specifica l'angolo in corrispondenza del quale il testo specificato con textPs= viene disposto e sottoposto a rendering nella casella di testo (definita con size= o textFlowPath=).
solution: Experience Manager
title: textAngle
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 102dbdc0-77b8-4c60-b456-6cf693e0b38b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# textAngle{#textangle}

Direzione rendering testo. Specifica l&#39;angolo in corrispondenza del quale il testo specificato con textPs= viene disposto e sottoposto a rendering nella casella di testo (definita con size= o textFlowPath=).

` textAngle= *`angolo`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> angolo </span> </p> </td> 
  <td class="stentry"> <p>Angolo di direzione (gradi). </p> </td> 
 </tr> 
</table>

I valori positivi ruotano il testo in senso orario; `textAngle=90` disegna il testo dall&#39;alto verso il basso.

## Proprietà {#section-6d586a632daa4261a8ce62db56140b36}

Attributo livello. Applicabile a `layer=0` se `layer=comp`. Ignorato se `textPs=` non è specificato per questo livello o se `textPath=` è specificato.

## Predefinito {#section-49a9f5819c994c27928282c14b2bb2a7}

`textAngle=0` senza rotazione.

## Consultate anche {#section-dccc29ff33704061b2519b56b7be45fd}

[Formattazione testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [Posizionamento testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
