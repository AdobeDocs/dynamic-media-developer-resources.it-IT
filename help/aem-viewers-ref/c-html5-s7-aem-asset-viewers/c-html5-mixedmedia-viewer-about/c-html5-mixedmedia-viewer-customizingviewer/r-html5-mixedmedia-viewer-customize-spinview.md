---
title: Visualizzazione a 360 gradi
description: La vista principale è costituita dall’immagine di rotazione quando la risorsa corrente è un set 360 gradi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aafc1299-b09a-4379-bd8f-b564066175bd
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo nel formato esadecimale della vista a rotazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la vista a rotazione.

```
.s7mixedmediaviewer .s7spinview { 
 background-color: transparent; 
}
```
