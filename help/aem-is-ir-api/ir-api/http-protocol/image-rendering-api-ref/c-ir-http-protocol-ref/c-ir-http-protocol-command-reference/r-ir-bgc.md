---
title: bgc
description: Colore di sfondo. Specifica il colore di sottrazione per le texture e le decalcomanie colorabili.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
TQID: 'https://experienceleague.adobe.com/0Er9kHrfQj1lt14SlNJHxqddJZOp8BaO-lLYSqc5ajU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 159
ht-degree: 2%

---

# bgc {#bgc}

Colore di sfondo. Specifica il colore di sottrazione per le texture e le decalcomanie colorabili.

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> colore</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>Valore di colore RGB o grigio. </p></td> 
 </tr> 
</table>

L&#39;algoritmo di colorizzazione della texture di Image Rendering è semplice: i valori dei componenti di `bgc=` vengono sottratti dai valori dei pixel della texture; viene aggiunto `color=` e infine il risultato viene ritagliato su `0,0,0` e `255,255,255`.

Per gli usi tipici della colorizzazione delle texture, il valore per `bgc=` potrebbe essere il colore più importante o dominante nell&#39;immagine della texture. Dynamic Media Image Authoring fornisce strumenti semi-automatici che estraggono ragionevoli valori di colore `bgc=` dalle immagini delle texture.

Quando un materiale di trama viene applicato a un oggetto di vignettatura non testurizzabile, `bgc=` viene applicato come colore di primo piano se `color=` non è specificato.

## Proprietà {#section-b2db6f147d7f443ba9f671de04c2ef19}

Attributo materiale. Ignorato dal colore a tinta unita e dai materiali dei cabinet.

## Predefinito {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` Se il materiale è basato su una voce di catalogo, altrimenti `bgc=808080` (grigio neutro).

## Esempio {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

Colorare un tessuto di abbigliamento la cui texture ha il colore dominante RGB 120,34,193:

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## Consultate anche {#section-de9958dd63a742b4b5d780c59a57da33}

[catalogo::BaseColor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) , [colore=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
