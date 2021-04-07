---
description: Riferimento API JavaScript per il visualizzatore di immagini video.
solution: Experience Manager
title: InteractiveImage
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Immagini interattive
role: Sviluppatore, Business Practices
exl-id: 165de14f-0031-4969-9671-5da310d44c28
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 3%

---

# InteractiveImage{#interactiveimage}

Riferimento API JavaScript per il visualizzatore di immagini video.

`InteractiveImage([config])`

Crea una nuova istanza del Visualizzatore immagini video.

## Parametri {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} oggetto di configurazione JSON  </span> opzionale, consente a tutte le impostazioni del visualizzatore di passare al costruttore per evitare di chiamare i singoli metodi del setter. Contiene le seguenti proprietà: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID del contenitore DOM (in genere un  <span class="codeph"> DIV  </span>) in cui viene inserito il visualizzatore. Quando si chiama questo metodo, non è necessario che l'elemento contenitore sia creato. Tuttavia, il contenitore deve esistere quando viene eseguito <span class="codeph"> init() </span> . </p> <p>Obbligatorio. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params  </span> - Oggetto  <span class="codeph"> {Object}  </span> JSON con parametri di configurazione del visualizzatore in cui il nome della proprietà è un’opzione di configurazione specifica per il visualizzatore o un modificatore SDK e il valore di tale proprietà è un valore di impostazioni corrispondente. </p> <p>Obbligatorio. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> gestori  </span> -  <span class="codeph"> {Object} oggetto  </span> JSON con callback di eventi del visualizzatore, dove il nome della proprietà è il nome dell'evento del visualizzatore supportato e il valore della proprietà è un riferimento alla funzione JavaScript per il callback appropriato. </p> <p>Facoltativo. </p> <p>Per ulteriori informazioni sugli eventi del visualizzatore, consulta <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> callback di eventi </a> . </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
  "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
} 
});
```
