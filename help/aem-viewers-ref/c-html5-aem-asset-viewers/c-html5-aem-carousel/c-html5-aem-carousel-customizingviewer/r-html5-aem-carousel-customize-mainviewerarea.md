---
title: Area visualizzatore principale
description: L’area di visualizzazione principale è l’area occupata dall’immagine del carosello. È impostato per adattarsi allo schermo del dispositivo disponibile quando non è specificata alcuna dimensione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: bdac54f5-79e3-4d3d-9c7e-d9a7cec61c73
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# Area visualizzatore principale{#main-viewer-area}

L’area di visualizzazione principale è l’area occupata dall’immagine del carosello. È impostato per adattarsi allo schermo del dispositivo disponibile quando non è specificata alcuna dimensione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato dal seguente selettore di classi CSS:

```
.s7carouselviewer
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo in formato esadecimale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un visualizzatore con sfondo bianco ( `#FFFFFF`) e impostarne le dimensioni a 1174 x 500 pixel.

```
.s7carouselviewer { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```
