---
title: qlt
description: Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 7%

---

# qlt{#qlt}

Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione.

` qlt= *`qualità`*[. *`crominanza`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> qualità </span> </p> </td> 
  <td class="stentry"> <p>Qualità codifica JPEG (1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> crominanza </span> </p> </td> 
  <td class="stentry"> <p>Downsampling cromaticità JPEG (0=normale, 1=disattivato); facoltativo, valore predefinito: 0. </p> </td> 
 </tr> 
</table>

Specifica gli attributi di codifica JPEG per controllare il livello di compressione. A sua volta, questo varia la dimensione del file (quantità di dati di risposta) e, indirettamente, la qualità visiva dell&#39;immagine risultante.

Valori più alti di *`quality`* aumentano le dimensioni e la qualità del file, valori più bassi riducono le dimensioni dei file e riducono la qualità percepita delle immagini. Con valori superiori a 90 si ottengono spesso immagini molto simili alle corrispondenti immagini non compresse.

Impostare il flag *`chroma`* per disattivare il downsampling della cromaticità utilizzato dai tipici encoder JPEG. Questa impostazione può aumentare la nitidezza percepita dei bordi di un&#39;immagine quando il bordo è definito da una variazione di tonalità anziché di luminosità. L&#39;impostazione di questo flag può causare un leggero aumento delle dimensioni del file. Provare con questa impostazione se il testo sembra leggermente sfocato.

## Proprietà {#section-897b61c786dd4230a2c5807f2f40e722}

Può verificarsi ovunque nella richiesta.

Ignorato se il formato dell&#39;immagine di output non supporta la compressione JPEG. Fare riferimento alla descrizione di `fmt=` per un elenco dei formati di immagine di output che supportano la compressione JPEG.

## Predefinito {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## Consultate anche {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attributo::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
