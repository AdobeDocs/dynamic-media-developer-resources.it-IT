---
title: qlt
description: Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (quantità di dati di risposta) e, indirettamente, la qualità visiva dell'immagine risultante.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
TQID: 'https://experienceleague.adobe.com/e7zzYHSi7X5tdPAy-0CWTK-Wqs5nfhEDLs2HYJ1D-f4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 242
ht-degree: 6%

---

# qlt{#qlt}

Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (quantità di dati di risposta) e, indirettamente, la qualità visiva dell&#39;immagine risultante.

` qlt= *`qualità`*[, *`crominanza`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> qualità </span> </p> </td> 
  <td class="stentry"> <p>Qualità della codifica JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> crominanza </span> </p> </td> 
  <td class="stentry"> <p>Downsampling cromaticità JPEG (0=normale, 1=disattivato); facoltativo, valore predefinito: 0. </p> </td> 
 </tr> 
</table>

Valori più alti di *`quality`* aumentano le dimensioni e la qualità del file, valori più bassi riducono le dimensioni dei file e riducono la qualità percepita delle immagini. Con valori superiori a 90 si ottengono spesso immagini molto simili alle corrispondenti immagini non compresse.

Impostare il flag *`chroma`* per disattivare il downsampling della cromaticità RGB utilizzato dai tipici encoder JPEG. Questo può aumentare la nitidezza percepita dei bordi di un&#39;immagine quando il bordo è definito da una variazione di tonalità piuttosto che di luminosità. L&#39;impostazione di questo flag può causare un leggero aumento delle dimensioni del file. Provare con questa impostazione se il testo sembra leggermente sfocato.

## Proprietà {#section-925a44cbdc9042db8d4eb149cd073d21}

Attributo della richiesta. Si applica indipendentemente dall&#39;impostazione del livello corrente. Ignorato se il formato del file di immagine di output non supporta la codifica JPEG. Fare riferimento alla descrizione di `fmt=` per informazioni sui formati immagine di output che supportano `qlt=`.

*`chroma`* viene ignorato se il tipo di pixel di output è CMYK o grigio.

## Predefinito {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Esempio {#section-d7d33871d401433aa51d028823eae7a9}

Ridurre la qualità per una trasmissione più rapida attraverso una connessione a bassa larghezza di banda:

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Aumento della qualità per connessioni a banda larga:

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Consultate anche {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attributo::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
