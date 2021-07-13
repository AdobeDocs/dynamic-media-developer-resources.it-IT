---
description: Attributi del testo sul percorso.
solution: Experience Manager
title: pathAttr
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 3%

---

# pathAttr{#pathattr}

Attributi del testo sul percorso.

` pathAttr= *``*[, *``*[, *`directionstartPosendPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> direzione </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norma  </span> |  <span class="codeph"> inverso  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos  </span> </p> </td> 
  <td class="stentry"> <p>Posizione iniziale testo sul percorso (reale 0.0...1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos  </span> </p> </td> 
  <td class="stentry"> <p>Posizione finale del testo sul percorso (reale 0.0...&lt;2.0). </p> </td> 
 </tr> 
</table>

Specificare `norm` per disegnare il testo partendo dal primo vertice del tracciato e `reverse` per disegnare il testo nella direzione opposta, partendo dall&#39;ultimo vertice.

*`startPos`* e  *`endPos`* consentire la regolazione del punto in cui verrà tracciato il testo. 0,0 corrisponde al primo vertice del percorso e 1,0 all’ultimo vertice; i valori intermedi esprimono la distanza lungo il percorso tra il primo e l&#39;ultimo vertice.

## Proprietà {#section-80f266da4e2549d89f022a3f9ff4584d}

Attributo livello. Ignorato se il livello non include i comandi `textPs=` e `textPath=`.

*`startPos`* deve essere maggiore o uguale a 0 e minore di 1.0.  *`endPos`* deve essere maggiore  *`startPos`* e minore o uguale a 1.0 se applicato a un percorso aperto, o minore o uguale a (  *`startPos`* + 1.0) se applicato a un percorso chiuso.

## Predefinito {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Consultate anche {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
