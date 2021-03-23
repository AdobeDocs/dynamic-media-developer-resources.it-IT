---
description: Qualità jpeg. Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (la quantità dei dati di risposta) e, indirettamente, la qualità visiva dell'immagine risultante.
seo-description: Qualità jpeg. Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (la quantità dei dati di risposta) e, indirettamente, la qualità visiva dell'immagine risultante.
seo-title: qlt
solution: Experience Manager
title: qlt
uuid: 936607c1-20c3-4f76-b970-614b21c47dea
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 12%

---


# qlt{#qlt}

Qualità jpeg. Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (la quantità dei dati di risposta) e, indirettamente, la qualità visiva dell&#39;immagine risultante.

` qlt= *``*[, *`qualitychroma`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> qualità  </span> </span> </p> </td> 
  <td class="stentry"> <p>Qualità di codifica JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> crominanza  </span> </span> </p> </td> 
  <td class="stentry"> <p>sottocampionamento della cromaticità JPEG (0=normale, 1=disattivato); facoltativo, il valore predefinito è 0. </p> </td> 
 </tr> 
</table>

Utilizzato solo se `fmt=jpg`. Ignorato altrimenti

Valori di qualità maggiori producono file di dimensione e qualità maggiore, mentre a valori di qualità inferiori corrispondono file di dimensioni inferiori e una qualità immagine percepita inferiore. Con valori superiori a 90 si ottengono spesso immagini molto simili alle corrispondenti immagini non compresse.

Impostare il flag `chroma` per disabilitare il campionamento per la cromaticità RGB utilizzato dai codificatori JPEG tipici. Questo può aumentare la nitidezza percepita dei bordi in un&#39;immagine quando il bordo è definito da un cambiamento di tonalità piuttosto che di luminosità. L’impostazione di questo flag può causare un leggero aumento delle dimensioni del file. Sperimenta questa impostazione se il testo sembra leggermente sfocato.

`chroma` viene ignorato se il tipo di pixel di output è CMYK o grigio.

## Esempio {#section-a6c263f15c29424a86ef267c96a6630a}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80]
