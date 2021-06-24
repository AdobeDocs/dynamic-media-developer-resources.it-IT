---
description: Modalità di ricampionamento. Seleziona l'algoritmo di ricampionamento e/o interpolazione da utilizzare per scalare l'immagine renderizzata alle dimensioni specificate con wid=, hei= o scl=.
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 13%

---

# resMode{#resmode}

Modalità di ricampionamento. Seleziona l&#39;algoritmo di ricampionamento e/o interpolazione da utilizzare per scalare l&#39;immagine renderizzata alle dimensioni specificate con wid=, hei= o scl=.

` `resMode=bilin|bicub|Sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>Seleziona l'interpolazione bilineare standard. È il metodo di ricampionamento più veloce; possono essere visibili alcuni artefatti di alias. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Seleziona l'interpolazione bicubica. Maggiore utilizzo della CPU rispetto all'interpolazione bilineare, ma produrrà immagini più nitide con artefatti di aliasing meno evidenti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> diesis2  </span> </p> </td> 
   <td colname="col2"> <p>come algoritmo di interpolazione viene utilizzata una funzione Lanczos Window modificata. Può produrre risultati leggermente più nitidi rispetto a bicubici a un costo di CPU più elevato. </p> <p> <span class="codeph"> diesis  </span> è stato sostituito da  <span class="codeph"> Sharp2  </span>, che ha una probabilità minore di causare artefatti di aliasing, noto anche come Moiré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vescovo  </span> </p> </td> 
   <td colname="col2"> <p>Seleziona il <span class="keyword"> campionatore predefinito Adobe Photoshop </span> per ridurre le dimensioni dell'immagine, denominato "più nitida bicubica" in <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-ea7029f37e094d9cb85646b85fbac0ce}

Può verificarsi in qualsiasi punto della richiesta. Ignorato se non viene applicata alcuna scala immagine finale.

## Predefinito {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Consultate anche {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attributo::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
