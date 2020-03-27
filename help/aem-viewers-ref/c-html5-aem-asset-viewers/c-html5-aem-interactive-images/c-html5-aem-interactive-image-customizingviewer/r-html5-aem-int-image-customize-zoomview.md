---
description: La vista principale è costituita dall’immagine statica.
seo-description: La vista principale è costituita dall’immagine statica.
seo-title: Visualizzazione zoom
solution: Experience Manager
title: Visualizzazione zoom
topic: Dynamic media
uuid: d8349f8c-134f-4e74-9d0c-ab56981965d7
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoom view{#zoom-view}

La vista principale è costituita dall’immagine statica.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;area di visualizzazione è controllato dal seguente selettore di classe CSS:

```
.s7interactiveimage .s7zoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo nel formato esadecimale della vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la vista principale.

```
.s7interactiveimage .s7zoomview { 
 background-color: transparent; 
}
```

