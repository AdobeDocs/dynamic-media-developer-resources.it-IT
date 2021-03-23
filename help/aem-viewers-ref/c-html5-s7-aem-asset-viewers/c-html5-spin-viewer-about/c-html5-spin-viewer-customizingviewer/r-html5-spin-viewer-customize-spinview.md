---
description: La vista principale è costituita dall’immagine di rotazione.
seo-description: La vista principale è costituita dall’immagine di rotazione.
seo-title: Visualizzazione a 360 gradi
solution: Experience Manager
title: Visualizzazione a 360 gradi
uuid: 74f42373-b08c-43c8-8f08-e61a09655b61
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set 360 gradi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 1%

---


# Visualizzazione a 360 gradi{#spin-view}

La vista principale è costituita dall’immagine di rotazione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato con il seguente selettore di classe CSS:

```
.s7spinviewer .s7spinview
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
.s7spinviewer .s7spinview { 
 background-color: transparent; 
}
```

