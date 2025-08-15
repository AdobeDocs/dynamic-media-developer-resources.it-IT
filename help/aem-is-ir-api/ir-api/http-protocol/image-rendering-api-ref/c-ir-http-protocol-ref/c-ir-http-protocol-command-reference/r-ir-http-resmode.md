---
title: resMode
description: Metodo di ricampionamento. Seleziona l'algoritmo di ricampionamento e/o interpolazione da utilizzare per ridimensionare l'immagine sottoposta a rendering alle dimensioni specificate con wid=, hei= o scl=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 7%

---

# resMode{#resmode}

Metodo di ricampionamento. Seleziona l&#39;algoritmo di ricampionamento e/o interpolazione da utilizzare per ridimensionare l&#39;immagine sottoposta a rendering alle dimensioni specificate con `wid=`, `hei=` o `scl=`.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Seleziona l'interpolazione bilineare standard. È il metodo di ricampionamento più veloce; possono essere visibili alcuni artefatti di alias. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Seleziona l'interpolazione bicubica. L'interpolazione è più intensiva di CPU rispetto a quella bilineare, ma produce immagini più nitide con meno artefatti di aliasing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Seleziona una funzione Finestra di Lanczo modificata come algoritmo di interpolazione. Può produrre risultati leggermente più nitidi rispetto a bicubic a un costo CPU più elevato. </p> <p> <span class="codeph"> </span> è stato sostituito da <span class="codeph"> </span>, che ha meno probabilità di causare artefatti di alias, noti anche come Moiré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vescovo </span> </p> </td> 
   <td colname="col2"> <p>Seleziona il ricampionatore predefinito <span class="keyword"> di Adobe Photoshop </span> per la riduzione delle dimensioni dell'immagine, denominato "bicubic sharper" in <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-ea7029f37e094d9cb85646b85fbac0ce}

Può verificarsi ovunque all’interno della richiesta. Ignorato se non viene applicato alcun ridimensionamento finale dell&#39;immagine.

## Predefinito {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Consultate anche {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attributo::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
