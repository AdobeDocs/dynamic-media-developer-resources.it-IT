---
description: Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione.
seo-description: Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 46f5b0da-7fe7-4daf-947b-bb5f5f5f5e6d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 7%

---


# qlt{#qlt}

Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione.

` qlt= *`crominanza `*[. *`qualitativa`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Qualità </span> </p> </td> 
  <td class="stentry"> <p>Qualità di codifica JPEG (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> crominanza  </span> </p> </td> 
  <td class="stentry"> <p>downsampling della cromaticità JPEG (0=normale, 1=disattivato); facoltativo, il valore predefinito è 0. </p> </td> 
 </tr> 
</table>

Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (quantità dei dati di risposta) e, indirettamente, la qualità visiva dell’immagine risultante.

Valori *`quality`* più alti aumentano la dimensione e la qualità dei file, valori più bassi riducono le dimensioni dei file e riducono la qualità percepita dell&#39;immagine. Con valori superiori a 90 si ottengono spesso immagini molto simili alle corrispondenti immagini non compresse.

Impostate il flag *`chroma`* per disabilitare il downsampling della cromaticità utilizzato dai codificatori JPEG tipici. Questo può aumentare la nitidezza percepita dei bordi di un’immagine quando il bordo è definito da una modifica della tonalità anziché dalla luminosità. L&#39;impostazione di questo flag potrebbe causare un lieve aumento delle dimensioni del file. Sperimentate con questa impostazione se il testo sembra leggermente sfocato.

## Proprietà {#section-897b61c786dd4230a2c5807f2f40e722}

Può verificarsi ovunque nella richiesta.

Ignorato se il formato dell&#39;immagine di output non supporta la compressione JPEG. Fare riferimento alla descrizione di `fmt=` per un elenco dei formati immagine di output che supportano la compressione JPEG.

## Predefinito {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Consultate anche {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
