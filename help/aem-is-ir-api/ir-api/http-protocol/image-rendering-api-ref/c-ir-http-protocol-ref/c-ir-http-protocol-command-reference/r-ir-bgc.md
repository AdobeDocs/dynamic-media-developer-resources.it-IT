---
description: Colore di sfondo. Specifica il colore sottrattivo per le texture e le decorazioni colorabili.
seo-description: Colore di sfondo. Specifica il colore sottrattivo per le texture e le decorazioni colorabili.
seo-title: bgc
solution: Experience Manager
title: bgc
topic: Scene7 Image Serving - Image Rendering API
uuid: 551a0da8-dd1f-484a-bf7e-f4896370340a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# bgc{#bgc}

Colore di sfondo. Specifica il colore sottrattivo per le texture e le decorazioni colorabili.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>Valore colore RGB o grigio. </p></td> 
 </tr> 
</table>

L’algoritmo di colorizzazione della texture del rendering delle immagini è abbastanza semplice: i valori dei componenti di `bgc=` vengono sottratti da quelli dei pixel della texture, `color=` vengono aggiunti e infine il risultato viene ritagliato su `0,0,0` e `255,255,255`.

Per gli usi tipici della colorazione della texture, il valore per `bgc=` potrebbe essere il colore più importante o dominante nell’immagine della texture. Scene7 Image Authoring offre strumenti semi-automatici per l’estrazione di valori di `bgc=` colore ragionevoli dalle immagini di texture.

Quando un materiale texture viene applicato a un oggetto vignettatura non texture, `bgc=` viene applicato come colore di primo piano, se non `color=` viene specificato.

## Proprietà {#section-b2db6f147d7f443ba9f671de04c2ef19}

Attributo materiale. Ignorata dai materiali in tinta unita e cabinet.

## Predefinito {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` se il materiale è basato su una voce di catalogo, altrimenti `bgc=808080` (grigio neutro).

## Esempio {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Colorare un tessuto di abbigliamento la cui texture ha il colore RGB dominante 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Consultate anche {#section-de9958dd63a742b4b5d780c59a57da33}

[catalogo::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
