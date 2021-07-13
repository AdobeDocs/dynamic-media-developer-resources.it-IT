---
description: L’area di visualizzazione principale è l’area occupata dalla vista a comparsa e dai campioni.
solution: Experience Manager
title: Area visualizzatore principale
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Zoom in linea
role: Developer,User
exl-id: ab1653a3-38e6-49bb-97b7-005304349ec9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---

# Area visualizzatore principale{#main-viewer-area}

L’area di visualizzazione principale è l’area occupata dalla vista a comparsa e dai campioni.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato con il seguente selettore di classe CSS:

```
.s7flyoutviewer
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo in formato esadecimale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un visualizzatore a comparsa con sfondo bianco ( `#FFFFFF`) e impostarne le dimensioni di 260 x 500 pixel.

```
.s7flyoutviewer { 
 background-color: #FFFFFF; 
 width: 260px; 
 height: 500px;  
}
```
