---
description: L'area di visualizzazione principale è l'area occupata dal video 360. In genere è impostato per adattarsi alla schermata del dispositivo disponibile quando non è specificata alcuna dimensione.
solution: Experience Manager
title: Area visualizzatore principale
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video VR 360
role: Sviluppatore, Business Practices
exl-id: 912cb4b3-6409-48ed-9b9c-968b63718a1b
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# Area visualizzatore principale{#main-viewer-area}

L&#39;area di visualizzazione principale è l&#39;area occupata dal video 360. In genere è impostato per adattarsi alla schermata del dispositivo disponibile quando non è specificata alcuna dimensione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato con il seguente selettore di classe CSS:

```
.s7video360viewer
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

## Esempio {#section-ee18025b182a42dc98052de5f133ddfe}

Impostare un visualizzatore con sfondo bianco ( `#FFFFFF`) e ridimensionarlo di 512 x 288 pixel.

```
.s7video360viewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
