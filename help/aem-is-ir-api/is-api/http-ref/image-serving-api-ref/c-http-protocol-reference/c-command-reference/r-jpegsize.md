---
description: Dimensione JPEG in KiloBytes. Specifica la dimensione massima della risposta JPEG in kilobyte.
seo-description: Dimensione JPEG in KiloBytes. Specifica la dimensione massima della risposta JPEG in kilobyte.
seo-title: jpegSize
solution: Experience Manager
title: jpegSize
topic: Scene7 Image Serving - Image Rendering API
uuid: 832163ca-0554-481d-b87f-bf322f415274
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# jpegSize{#jpegsize}

Dimensione JPEG in KiloBytes. Specifica la dimensione massima della risposta JPEG in kilobyte.

`jpegSize= *`size`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> dimensione</span></span> </p> </td> 
  <td class="stentry"> <p>Dimensioni in kilobyte. </p></td> 
 </tr> 
</table>

Se questo è impostato su un valore positivo e la risposta JPEG con la qualità JPEG specificata non supera questo valore, l&#39;immagine viene restituita come risposta. In caso contrario, la qualità JPEG diminuisce finché non produce un’immagine che si adatta alle dimensioni specificate o finché non determina che non può essere adattata. In quest&#39;ultimo caso, la richiesta non riesce con un errore.

Il valore 0 indica che la risposta non è vincolata dalle dimensioni.

I valori negativi non sono consentiti.

## Proprietà {#section-19e544e77d35478b98fe8666f27d6968}

Attributo di richiesta. Si applica indipendentemente dall’impostazione del livello corrente. Ignorato se il formato immagine di output non è JPEG.

## Predefinito {#section-198b798ed187453197e0969c641d6fb5}

0

## Esempio {#section-46bf806fd3ef4875b7726df32b6f834d}

Le dimensioni della garanzia non sono eccessive per la distribuzione a un dispositivo con memoria limitata:

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## Consultate anche {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
