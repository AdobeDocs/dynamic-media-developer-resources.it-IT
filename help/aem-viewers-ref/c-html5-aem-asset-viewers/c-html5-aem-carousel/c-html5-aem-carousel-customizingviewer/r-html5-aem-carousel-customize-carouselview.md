---
description: La vista principale è costituita dall’immagine del banner.
solution: Experience Manager
title: Vista a carosello
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: aa41b209-11c7-4744-aaa5-dc0b503607c6
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 1%

---

# Vista a carosello{#carousel-view}

La vista principale è costituita dall’immagine del banner.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato con il seguente selettore di classe CSS:

```
.s7carouselviewer .s7carouselview
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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo nel formato esadecimale della vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio : per rendere trasparente la visualizzazione principale.

```
.s7carouselviewer .s7carouselview { 
 background-color: transparent; 
}
```
