---
description: Colore di sfondo. Specifica il colore sottrattivo per le texture e le decorazioni colorabili.
solution: Experience Manager
title: bgc
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 6%

---

# bgc{#bgc}

Colore di sfondo. Specifica il colore sottrattivo per le texture e le decorazioni colorabili.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>Valore del colore RGB o grigio. </p></td> 
 </tr> 
</table>

L&#39;algoritmo di colorazione della texture di Image Rendering è abbastanza semplice: i valori dei componenti di `bgc=` vengono sottratti da quelli dei pixel della texture, viene aggiunto `color=` e infine il risultato viene ritagliato su `0,0,0` e `255,255,255`.

Per gli usi tipici della colorazione della texture, il valore per `bgc=` potrebbe essere il colore più importante o dominante nell&#39;immagine della texture. Dynamic Media Image Authoring fornisce strumenti semi-automatici che estraggono valori di colore ragionevoli `bgc=` dalle immagini di texture.

Quando un materiale di texture viene applicato a un oggetto vignetta non testurizzabile, `bgc=` viene applicato come colore di primo piano se `color=` non è specificato.

## Proprietà {#section-b2db6f147d7f443ba9f671de04c2ef19}

Attributo materiale. Ignorato da colori solidi e materiali per armadietti.

## Predefinito {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` se il materiale è basato su una voce di catalogo, altrimenti  `bgc=808080` (grigio neutro).

## Esempio {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Colorare un tessuto di abbigliamento la cui texture ha il colore RGB dominante 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Consultate anche {#section-de9958dd63a742b4b5d780c59a57da33}

[catalogo::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) ,  [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
