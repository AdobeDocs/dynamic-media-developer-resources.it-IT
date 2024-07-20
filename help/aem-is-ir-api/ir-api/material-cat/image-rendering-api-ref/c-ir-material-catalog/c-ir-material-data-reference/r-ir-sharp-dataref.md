---
description: Nitidezza. Attributo di nitidezza, determina quando viene applicata la nitidezza al materiale durante il rendering.
solution: Experience Manager
title: Nitido
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce08ed97-33b7-4d28-8f7f-3f3ef8598ad6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 6%

---

# Nitido{#sharp}

Nitidezza. Attributo di nitidezza, determina quando viene applicata la nitidezza al materiale durante il rendering.

Il tipo e la quantità di nitidezza sono controllati dalla vignettatura tramite un modello di materiale predefinito o con `catalog::RenderSettings`.

## Proprietà {#section-aac81b1a611b4bca90b8544eae7896df}

Enum.

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Nessuna nitidezza. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Nitidezza normale (dopo la trasformazione). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Nitidezza alternativa (prima della trasformazione). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Maggiore nitidezza (sia prima che dopo la trasformazione). </p></td> 
 </tr> 
</table>

Ignorato dai materiali colorati, facoltativo per tutti gli altri materiali.

## Predefinito {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` viene utilizzato se il campo non è presente, se è vuoto o se il valore non è una delle scelte supportate.

## Consultate anche {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[attributo::Nitidezza](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) , [catalogo::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [nitidezza=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
