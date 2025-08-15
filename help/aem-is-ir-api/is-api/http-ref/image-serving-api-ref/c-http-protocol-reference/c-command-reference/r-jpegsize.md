---
title: Dimensione jpeg
description: Dimensione JPEG in kilobyte. Specifica la dimensione massima della risposta JPEG in kilobyte.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08cecb09-100f-4671-b335-d59c88b0e1ef
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# Dimensione jpeg{#jpegsize}

Dimensione JPEG in kilobyte. Specifica la dimensione massima della risposta JPEG in kilobyte.

`jpegSize= *`grandezza`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> grandezza</span></span> </p> </td> 
  <td class="stentry"> <p>Dimensioni in kilobyte. </p></td> 
 </tr> 
</table>

Se questo valore è impostato su un valore positivo e se la risposta JPEG con la qualità JPEG specificata non supera questo valore, tale immagine viene restituita come risposta. In caso contrario, la qualità JPEG diminuisce fino a quando non produce un&#39;immagine che si adatta alle dimensioni specificate o fino a quando non determina che non può adattarsi. In quest&#39;ultimo caso, l&#39;richiesta non riesce e restituisce un errore.

Il valore 0 indica che la risposta non è vincolata dalle dimensioni.

I valori negativi non sono consentiti.

## Proprietà {#section-19e544e77d35478b98fe8666f27d6968}

Attributo request. Si applica indipendentemente dall&#39;impostazione del livello corrente. Ignorato se il formato immagine di output non è JPEG.

## Predefinito {#section-198b798ed187453197e0969c641d6fb5}

0

## Esempio {#section-46bf806fd3ef4875b7726df32b6f834d}

Garantire che le dimensioni non siano troppo grandi per la distribuzione a un dispositivo con memoria limitata:

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## Consultate anche {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
