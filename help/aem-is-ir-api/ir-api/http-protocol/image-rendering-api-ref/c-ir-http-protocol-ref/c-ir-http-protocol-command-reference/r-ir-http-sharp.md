---
title: acuto
description: Texture più nitide. Specifica la nitidezza da applicare durante il rendering di questo materiale.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 5%

---

# acuto{#sharp}

Texture più nitide. Specifica la nitidezza da applicare durante il rendering di questo materiale.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Nessuna nitidezza. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Nitidezza normale (in ritardo). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 nitidezza alternativa (precoce). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Maggiore nitidezza (precoce e tardivo). </p> </td> 
 </tr> 
</table>

`sharp=1` Applica la nitidezza dopo il rendering del materiale; `sharp=2` applica la nitidezza dopo il ridimensionamento iniziale della texture, ma prima che questa venga trasformata nella scena; `sharp=3` applica la nitidezza sia prima che dopo la trasformazione.

L&#39;algoritmo di nitidezza e la quantità di nitidezza e altri parametri USM (Maschera di contrasto) sono controllati dal modello di materiale predefinito fornito dalla vignettatura o con `rs=`.

## Proprietà {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Attributo materiale. Ignorato dai materiali a colori.

## Predefinito {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, se il materiale è basato su una voce di catalogo, altrimenti `attribute::Sharp`.

## Consultate anche {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalogo::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharpen= nitidezza](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
