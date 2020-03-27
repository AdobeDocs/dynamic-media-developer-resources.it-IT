---
description: Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (quantità dei dati di risposta) e, indirettamente, la qualità visiva dell’immagine risultante.
seo-description: Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (quantità dei dati di risposta) e, indirettamente, la qualità visiva dell’immagine risultante.
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 936607c1-20c3-4f76-b970-614b21c47dea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# qlt{#qlt}

Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (quantità dei dati di risposta) e, indirettamente, la qualità visiva dell’immagine risultante.

` qlt= *`crominanza`*[, *`qualitativa`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> qualità </span></span> </p> </td> 
  <td class="stentry"> <p>Qualità di codifica JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> crominanza </span></span> </p> </td> 
  <td class="stentry"> <p>downsampling della cromaticità JPEG (0=normale, 1=disattivato); facoltativo, il valore predefinito è 0. </p> </td> 
 </tr> 
</table>

Utilizzata solo se `fmt=jpg`. Ignorato altrimenti

Valori di qualità maggiori producono file di dimensione e qualità maggiore, mentre a valori di qualità inferiori corrispondono file di dimensioni inferiori e una qualità immagine percepita inferiore. Con valori superiori a 90 si ottengono spesso immagini molto simili alle corrispondenti immagini non compresse.

Impostate il `chroma` flag per disabilitare il downsampling della cromaticità RGB utilizzato dai codificatori JPEG tipici. Questo può aumentare la nitidezza percepita dei bordi di un’immagine quando il bordo è definito da una modifica della tonalità anziché dalla luminosità. L&#39;impostazione di questo flag potrebbe causare un lieve aumento delle dimensioni del file. Sperimentate con questa impostazione se il testo sembra leggermente sfocato.

`chroma` viene ignorato se il tipo di pixel di output è CMYK o grigio.

## Esempio {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
