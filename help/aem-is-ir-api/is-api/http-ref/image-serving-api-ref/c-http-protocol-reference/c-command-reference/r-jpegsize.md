---
title: jpegSize
description: Dimensione JPEG in kilobyte. Specifica la dimensione massima della risposta JPEG in kilobyte.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08cecb09-100f-4671-b335-d59c88b0e1ef
TQID: 'https://experienceleague.adobe.com/FXPTcUoMZP-mA-PyuaLqLFqqY9ITLWkjWgezRFUDiHI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 3%

---

# jpegSize{#jpegsize}

Dimensione JPEG in kilobyte. Specifica la dimensione massima della risposta JPEG in kilobyte.

`jpegSize= *`dimensioni`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Dimensione <span class="codeph"> <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>Dimensione in kilobyte. </p></td> 
 </tr> 
</table>

Se è impostato su un valore positivo e la risposta di JPEG con la qualità di JPEG specificata non supera questo valore, l’immagine viene restituita come risposta. In caso contrario, la qualità del JPEG diminuisce fino a quando non produce un&#39;immagine che si adatta alle dimensioni specificate o fino a quando non determina che non può rientrare. In quest’ultimo caso, la richiesta non riesce e viene visualizzato un errore.

Il valore 0 indica che la risposta non è vincolata dalla dimensione.

Non sono consentiti valori negativi.

## Proprietà {#section-19e544e77d35478b98fe8666f27d6968}

Attributo della richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente. Ignorato se il formato dell&#39;immagine di output non è JPEG.

## Predefinito {#section-198b798ed187453197e0969c641d6fb5}

0

## Esempio {#section-46bf806fd3ef4875b7726df32b6f834d}

Le dimensioni della garanzia non sono eccessive per la consegna a un dispositivo con memoria limitata:

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## Consultate anche {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attributo::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
