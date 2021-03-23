---
description: La vista principale è costituita dall’immagine di rotazione quando la risorsa corrente è un set 360 gradi.
seo-description: La vista principale è costituita dall’immagine di rotazione quando la risorsa corrente è un set 360 gradi.
seo-title: Visualizzazione a 360 gradi
solution: Experience Manager
title: Visualizzazione a 360 gradi
uuid: f1edbcc4-966a-4ec6-8ba9-a76f3ae51733
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---


# Visualizzazione a 360 gradi{#spin-view}

La vista principale è costituita dall’immagine di rotazione quando la risorsa corrente è un set 360 gradi.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato con il seguente selettore di classe CSS:

```
.s7mixedmediaviewer .s7spinview
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
   <td colname="col2"> <p> Colore di sfondo nel formato esadecimale della vista a rotazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la visualizzazione a rotazione.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```

