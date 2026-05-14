---
title: qlt
description: Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (quantità di dati di risposta) e, indirettamente, la qualità visiva dell'immagine risultante.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8801a650-303c-47a3-8136-c8b2b7a80e9d
TQID: 'https://experienceleague.adobe.com/sf3ydtf3lGCG1BfJfc1vW5hXFBawbeWJwXNSJdUEei8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 15%

---

# qlt{#qlt}

Qualità JPEG. Specifica gli attributi di codifica JPEG per controllare il livello di compressione. Questo a sua volta varia la dimensione del file (quantità di dati di risposta) e, indirettamente, la qualità visiva dell&#39;immagine risultante.

` qlt= *`Qualità`*[, *`crominanza`*]`

<table id="simpletable_D080D15922CE4EF4B707282A4D45739A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> qualità </span> </span> </p> </td> 
  <td class="stentry"> <p>Qualità della codifica JPEG (1...100 int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> crominanza </span> </span> </p> </td> 
  <td class="stentry"> <p>Downsampling cromaticità JPEG (0=normale, 1=disattivato); facoltativo, valore predefinito: 0. </p> </td> 
 </tr> 
</table>

Utilizzato solo se `fmt=jpg`. Ignorato altrimenti

Valori di qualità maggiori producono file di dimensione e qualità maggiore, mentre a valori di qualità inferiori corrispondono file di dimensioni inferiori e una qualità immagine percepita inferiore. Con valori superiori a 90 si ottengono spesso immagini molto simili alle corrispondenti immagini non compresse.

Impostare il flag `chroma` per disattivare il downsampling della cromaticità RGB utilizzato dai tipici encoder JPEG. Questo può aumentare la nitidezza percepita dei bordi di un&#39;immagine quando il bordo è definito da una variazione di tonalità piuttosto che di luminosità. L&#39;impostazione di questo flag può causare un leggero aumento delle dimensioni del file. Provare con questa impostazione se il testo sembra leggermente sfocato.

`chroma` viene ignorato se il tipo di pixel di output è CMYK o grigio.

## Esempio {#section-a6c263f15c29424a86ef267c96a6630a}

`http://server/is/agm/myRootId/myImageId?fmt=jpg&qlt=80`
