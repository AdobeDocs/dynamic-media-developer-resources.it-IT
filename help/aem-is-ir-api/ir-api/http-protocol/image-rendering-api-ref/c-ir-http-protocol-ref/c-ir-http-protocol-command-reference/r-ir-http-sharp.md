---
description: Nitidezza della texture. Specifica la nitidezza da applicare durante il rendering del materiale.
seo-description: Nitidezza della texture. Specifica la nitidezza da applicare durante il rendering del materiale.
seo-title: sharp
solution: Experience Manager
title: sharp
topic: Scene7 Image Serving - Image Rendering API
uuid: 8265eebf-9cec-4ad3-8b22-0f46f33a89f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sharp{#sharp}

Nitidezza della texture. Specifica la nitidezza da applicare durante il rendering del materiale.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Nessuna nitidezza. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Nitidezza normale (tardiva). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 nitidezza alternativa (nelle prime fasi). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Maggiore nitidezza (presto e tardi). </p> </td> 
 </tr> 
</table>

`sharp=1` applica la nitidezza dopo la riproduzione del materiale; applica `sharp=2` la nitidezza dopo il ridimensionamento iniziale della texture, ma prima di trasformarla in scena; applica `sharp=3` la nitidezza sia prima che dopo la trasformazione.

L’algoritmo di nitidezza e la quantità di nitidezza e altri parametri USM (maschera di contrasto) sono controllati dal modello di materiale predefinito fornito dalla vignettatura o con `rs=`.

## Proprietà {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Attributo materiale. Ignorata dai materiali in tinta unita.

## Predefinito {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, se il materiale è basato su una voce di catalogo, altrimenti `attribute::Sharp`.

## Consultate anche {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalogo::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
