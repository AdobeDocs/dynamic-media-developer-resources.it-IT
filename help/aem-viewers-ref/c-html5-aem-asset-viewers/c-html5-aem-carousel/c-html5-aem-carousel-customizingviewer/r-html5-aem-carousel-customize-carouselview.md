---
description: La vista principale è costituita dall'immagine del banner.
seo-description: La vista principale è costituita dall'immagine del banner.
seo-title: Vista carosello
solution: Experience Manager
title: Vista carosello
topic: Dynamic media
uuid: bf2065cc-fef2-4d4e-ab2a-a533fa063a80
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 1%

---


# Vista carosello{#carousel-view}

La vista principale è costituita dall&#39;immagine del banner.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;area di visualizzazione è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo nel formato esadecimale della vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la vista principale.

```
.s7carouselviewer .s7carouselview { 
 background-color: transparent; 
}
```

