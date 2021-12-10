---
title: Area visualizzatore principale
description: L'area di visualizzazione principale è l'area occupata dall'immagine dello zoom e dai campioni. In genere viene impostato per adattarsi alla schermata del dispositivo disponibile quando non viene specificata alcuna dimensione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 62cbb3e6-e766-40a3-9c01-d22ade82b604
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# Area visualizzatore principale{#main-viewer-area}

L&#39;area di visualizzazione principale è l&#39;area occupata dall&#39;immagine dello zoom e dai campioni. In genere viene impostato per adattarsi alla schermata del dispositivo disponibile quando non viene specificata alcuna dimensione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Quando si lavora in modalità incorporata (quando si assegna una dimensione esplicita all’area del visualizzatore principale), il visualizzatore diminuisce automaticamente l’altezza dell’area principale in base all’altezza del componente Campioni che funziona con la singola immagine e, pertanto, i campioni non sono necessari.

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato con il seguente selettore di classe CSS:

```
.s7zoomviewer
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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo in formato esadecimale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un visualizzatore con sfondo bianco ( `#FFFFFF`) e le sue dimensioni 512 x 288 pixel.

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
