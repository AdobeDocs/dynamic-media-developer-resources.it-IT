---
description: L’area di visualizzazione principale è l’area occupata dall’immagine di zoom e dai campioni. In genere viene impostato per adattarsi allo schermo del dispositivo disponibile quando non vengono specificate dimensioni.
seo-description: L’area di visualizzazione principale è l’area occupata dall’immagine di zoom e dai campioni. In genere viene impostato per adattarsi allo schermo del dispositivo disponibile quando non vengono specificate dimensioni.
seo-title: Area visualizzatore principale
solution: Experience Manager
title: Area visualizzatore principale
topic: Dynamic media
uuid: 689116cb-bbb9-4e26-9c16-9229330c4034
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Area visualizzatore principale{#main-viewer-area}

L’area di visualizzazione principale è l’area occupata dall’immagine di zoom e dai campioni. In genere viene impostato per adattarsi allo schermo del dispositivo disponibile quando non vengono specificate dimensioni.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Quando lavorate in modalità incorporata (quando viene data una dimensione esplicita all’area del visualizzatore principale), il visualizzatore riduce automaticamente l’altezza della sua area principale per l’altezza del componente Campioni che utilizza la singola immagine e, di conseguenza, i campioni non sono necessari.

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;area di visualizzazione è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo in formato esadecimale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un visualizzatore con uno sfondo bianco ( `#FFFFFF`) e impostarne le dimensioni di 512 x 288 pixel.

```
.s7zoomviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

