---
description: Attributi del testo sul tracciato.
seo-description: Attributi del testo sul tracciato.
seo-title: pathAttr
solution: Experience Manager
title: pathAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: b0ca5821-ee08-4c18-919d-775b75f19acd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 3%

---


# pathAttr{#pathattr}

Attributi del testo sul tracciato.

` pathAttr= *``*[, *``*[, *`directionstartPosendPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> direzione </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norma  </span> |  <span class="codeph"> inverso  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos  </span> </p> </td> 
  <td class="stentry"> <p>Posizione iniziale testo sul percorso (0.0...1.0 reale). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos  </span> </p> </td> 
  <td class="stentry"> <p>Posizione finale del testo sul percorso (0.0...&lt;2.0). </p> </td> 
 </tr> 
</table>

Specificare `norm` per disegnare il testo partendo dal primo vertice del tracciato e `reverse` per disegnare il testo nella direzione opposta, partendo dall&#39;ultimo vertice.

*`startPos`* e  *`endPos`* consentire la regolazione della posizione sul tracciato in cui verrà disegnato il testo. 0,0 corrisponde al primo vertice del tracciato e 1,0 all’ultimo vertice; i valori intermedi indicano la distanza lungo il percorso tra il primo e l’ultimo vertice.

## Proprietà {#section-80f266da4e2549d89f022a3f9ff4584d}

Attributo layer. Ignorato se il livello non include i comandi `textPs=` e `textPath=`.

*`startPos`* deve essere maggiore o uguale a 0 e minore di 1.0.  *`endPos`* deve essere maggiore  *`startPos`* e minore o uguale a 1.0 se applicato a un tracciato aperto, o minore o uguale a (  *`startPos`* + 1.0) se applicato a un tracciato chiuso.

## Predefinito {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Consultate anche {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
