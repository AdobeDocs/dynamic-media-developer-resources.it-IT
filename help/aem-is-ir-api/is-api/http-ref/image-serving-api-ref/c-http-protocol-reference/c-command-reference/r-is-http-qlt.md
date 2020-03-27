---
description: Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (quantità dei dati di risposta) e, indirettamente, la qualità visiva dell’immagine risultante.
seo-description: Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (quantità dei dati di risposta) e, indirettamente, la qualità visiva dell’immagine risultante.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f69845d-3b25-41a7-b6c0-83cf1d2bc450
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# qlt{#qlt}

Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (quantità dei dati di risposta) e, indirettamente, la qualità visiva dell’immagine risultante.

` qlt= *`crominanza`*[, *`qualitativa`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Qualità </span> </p> </td> 
  <td class="stentry"> <p>Qualità di codifica JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> crominanza </span> </p> </td> 
  <td class="stentry"> <p>downsampling della cromaticità JPEG (0=normale, 1=disattivato); facoltativo, il valore predefinito è 0. </p> </td> 
 </tr> 
</table>

Higher *`quality`* values increase file size and quality, lower values decrease file sizes and reduce perceived image quality. Con valori superiori a 90 si ottengono spesso immagini molto simili alle corrispondenti immagini non compresse.

Impostate il *`chroma`* flag per disabilitare il downsampling della cromaticità RGB utilizzato dai codificatori JPEG tipici. Questo può aumentare la nitidezza percepita dei bordi di un’immagine quando il bordo è definito da una modifica della tonalità anziché dalla luminosità. L&#39;impostazione di questo flag potrebbe causare un lieve aumento delle dimensioni del file. Sperimentate con questa impostazione se il testo sembra leggermente sfocato.

## Proprietà {#section-925a44cbdc9042db8d4eb149cd073d21}

Attributo di richiesta. Si applica indipendentemente dall’impostazione del livello corrente. Ignorato se il formato del file immagine di output non supporta la codifica JPEG. Fare riferimento alla descrizione di `fmt=` per informazioni sui formati di immagine di output supportati `qlt=`.

*`chroma`* viene ignorato se il tipo di pixel di output è CMYK o grigio.

## Predefinito {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## Esempio {#section-d7d33871d401433aa51d028823eae7a9}

Qualità ridotta per una trasmissione più rapida attraverso una connessione a banda larga ridotta:

`http://server/myRoodId/myImageId?qlt=60&wid=300`

Aumenta la qualità per connessioni a larghezza di banda elevata:

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## Consultate anche {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [attribute::JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
