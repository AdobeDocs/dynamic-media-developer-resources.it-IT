---
description: Maschera di contrasto. Maschere di contrasto del livello o dell'immagine di visualizzazione finale, dopo tutte le operazioni di ridimensionamento, se layer=comp.
solution: Experience Manager
title: op_usmR
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 51a779be-568b-40e5-99d9-e875023a2b2c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---

# op_usmR{#op-usmr}

Maschera di contrasto. Maschere di contrasto del livello o dell&#39;immagine di visualizzazione finale, dopo tutte le operazioni di ridimensionamento, se layer=comp.

I parametri vengono applicati così come sono, indipendentemente dal fatto che si sia verificato un downsampling.

`op_usmR= *`quantità`*[, *`raggioR`*[, *`soglia`*[, *`monocromatico`*]]]`

<table id="simpletable_0697E3BCB45F41C494D93A6017ADD2BF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> quantità</span></span> </p></td> 
  <td class="stentry"> <p>Fattore di intensità del filtro (reale 0...5). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> raggioR</span></span> </p></td> 
  <td class="stentry"> <p>Raggio kernel del filtro in pixel (reale 0...250). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> soglia</span></span> </p></td> 
  <td class="stentry"> <p>Livello soglia filtro (int 0...255). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> monocromatico</span></span> </p></td> 
  <td class="stentry"> <p>Impostate questo valore su 0 per applicarlo separatamente a ogni componente di colore, oppure su 1 per applicarlo solo alla luminosità (intensità) dell'immagine. </p> <p><span class="codeph"> <span class="varname"> monocromatico</span></span> viene ignorato per le immagini in scala di grigio. </p> </td> 
 </tr> 
</table>

Anche la maschera di livello o la maschera composita viene resa più nitida.

## Proprietà {#section-fb5311b34d164946b74dadb32359518a}

Attributo di livello o attributo di visualizzazione. Si applica al livello corrente o all&#39;immagine della vista finale se `layer=comp`. I livelli degli effetti lo ignorano.

## Predefinito {#section-2bedc99866ff473e90e5ea36596d8362}

`op_usmR=0,0,0,0` senza effetto di maschera di contrasto.

## Consultate anche {#section-63f186b8a1b34ec4bb895230838502a4}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_sharpen=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541) , [op_usm](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa)
