---
description: I valori di colore per gli attributi color= e bgc= possono essere specificati utilizzando un elenco di valori di componenti decimali, separati da virgole o una notazione esadecimale, simile a HTML.
solution: Experience Manager
title: Valori colore
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 11%

---


# Valori colore{#color-values}

I valori di colore per gli attributi color= e bgc= possono essere specificati utilizzando un elenco di valori di componenti decimali, separati da virgole o una notazione esadecimale, simile a HTML.

<table id="simpletable_9B3A231D5BB14A3DB2B42B341E198341"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> color</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">{ {rosso , verde , blu} | grigio } | { [ 0x ] esex6 } | { 0xhex2 }</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>rosso, verde, blu, grigio</i> </p></td> 
  <td class="stentry"> <p>Valore componente colore (0...255, numero intero decimale). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>ex6</i> </p></td> 
  <td class="stentry"> <p>Valore di colore RGB esadecimale a sei cifre (RRGGBB). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><i>ex2</i> </p></td> 
  <td class="stentry"> <p>Valore di colore grigio esadecimale a due cifre (0...FF). </p></td> 
 </tr> 
</table>

## Esempi {#section-a78732151d584e84abeb99f9ce8d7c24}

Alcuni esempi di identificatori di colore validi e la relativa interpretazione del valore del colore RGB:

<table id="simpletable_837B3173020240A5B7B2DB2F4CC57352"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0.100.200 </p></td> 
  <td class="stentry"> <p>(0.100.200) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>128 </p></td> 
  <td class="stentry"> <p>(128.128.128) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0x010203 </p></td> 
  <td class="stentry"> <p>(1,2,3) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>00b1c2 </p></td> 
  <td class="stentry"> <p>(160.177.194) </p></td> 
 </tr> 
</table>

## Consultate anche {#section-207d5cb918a94736a27445faa58917d3}

[color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa),  [bgc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-bgc.md#reference-3f5c78cea01c4a85aa582076d23aebb0),  [grout=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
