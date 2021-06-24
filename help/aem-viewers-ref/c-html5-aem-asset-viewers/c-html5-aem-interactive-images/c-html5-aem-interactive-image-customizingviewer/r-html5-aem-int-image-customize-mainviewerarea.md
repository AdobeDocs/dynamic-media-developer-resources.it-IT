---
description: L'area di visualizzazione principale è l'area occupata dall'immagine dello zoom. In genere è impostato per adattarsi alla schermata del dispositivo disponibile quando non è specificata alcuna dimensione.
solution: Experience Manager
title: Area visualizzatore principale
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Immagini interattive
role: Developer,Business Practitioner
exl-id: c8005e7e-dff6-4f40-a94c-6fb6640e827f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# Area visualizzatore principale{#main-viewer-area}

L&#39;area di visualizzazione principale è l&#39;area occupata dall&#39;immagine dello zoom. In genere è impostato per adattarsi alla schermata del dispositivo disponibile quando non è specificata alcuna dimensione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato con il seguente selettore di classe CSS:

```
.s7interactiveimage
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

Esempio: per impostare un visualizzatore con sfondo bianco ( `#FFFFFF`) e impostarne le dimensioni a 1174 x 500 pixel.

```
.s7interactiveimage { 
 background-color: #FFFFFF; 
 width: 1174px; 
 height: 500px;  
}
```
