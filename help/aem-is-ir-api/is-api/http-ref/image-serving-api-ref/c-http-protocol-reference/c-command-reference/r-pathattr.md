---
title: pathAttr
description: Attributi testo su tracciato.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---

# pathAttr{#pathattr}

Attributi testo su tracciato.

` pathAttr= *`direzione`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> direzione </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norma </span> | <span class="codeph"> inverso </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>Posizione iniziale del testo sul percorso (reale 0,0...1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>Posizione finale del testo sul percorso (reale 0,0...&lt;2,0). </p> </td> 
 </tr> 
</table>

Specifica `norm` per disegnare il testo che inizia vicino al primo vertice del tracciato e `reverse` per disegnare il testo nella direzione opposta, a partire dall&#39;ultimo vertice.

*`startPos`* e *`endPos`* consente di regolare la posizione sul tracciato in cui viene disegnato il testo. 0,0 corrisponde al primo vertice del tracciato e 1,0 all&#39;ultimo vertice; i valori intermedi esprimono la distanza lungo il tracciato tra il primo e l&#39;ultimo vertice.

## Proprietà {#section-80f266da4e2549d89f022a3f9ff4584d}

Attributo livello. Ignorato se il livello non include `textPs=` e `textPath=` comandi.

*`startPos`* deve essere maggiore o uguale a 0 e minore di 1,0. *`endPos`* deve essere maggiore di *`startPos`* e minore o uguale a 1,0 se applicato a un tracciato aperto o minore o uguale a ( *`startPos`* + 1.0) se applicata a un tracciato chiuso.

## Predefinito {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Consultate anche {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
