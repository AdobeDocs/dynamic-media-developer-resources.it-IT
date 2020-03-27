---
description: Modalità di ricampionamento. Seleziona l’algoritmo di ricampionamento e/o interpolazione da usare per ridimensionare l’immagine di cui è stato effettuato il rendering nelle dimensioni specificate con wid=, hei= o scl=.
seo-description: Modalità di ricampionamento. Seleziona l’algoritmo di ricampionamento e/o interpolazione da usare per ridimensionare l’immagine di cui è stato effettuato il rendering nelle dimensioni specificate con wid=, hei= o scl=.
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 106da74a-d7da-4998-a719-c4c69ae36f6b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# resMode{#resmode}

Modalità di ricampionamento. Seleziona l’algoritmo di ricampionamento e/o interpolazione da usare per ridimensionare l’immagine di cui è stato effettuato il rendering nelle dimensioni specificate con wid=, hei= o scl=.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Seleziona l’interpolazione bilineare standard. È il metodo di ricampionamento più veloce; possono essere visibili alcuni artefatti di alias. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Seleziona l’interpolazione bicubica. Richiede maggiore utilizzo della CPU rispetto all’interpolazione bilineare, ma produce immagini più nitide con meno artefatti di alias. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>come algoritmo di interpolazione viene utilizzata una funzione Lanczos Window modificata. Può produrre risultati leggermente più nitidi rispetto al bicubico a un costo CPU più elevato. </p> <p> <span class="codeph"> sharp </span> è stato sostituito da <span class="codeph"> sharp2 </span>, che ha una minore probabilità di artefatti di aliasing, noti anche come Moiré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Seleziona il <span class="keyword"> ricampionamento predefinito di Adobe Photoshop </span> per ridurre le dimensioni dell’immagine, che in <span class="keyword"> </span>Adobe Photoshop è denominato "bicubico più nitido". </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-ea7029f37e094d9cb85646b85fbac0ce}

Può verificarsi ovunque nella richiesta. Ignorato se non viene applicato il ridimensionamento dell’immagine finale.

## Predefinito {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Consultate anche {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
