---
description: Riferimento API JavaScript per il visualizzatore zoom.
seo-description: Riferimento API JavaScript per il visualizzatore zoom.
seo-title: ZoomViewer
solution: Experience Manager
title: ZoomViewer
topic: Dynamic media
uuid: 4c2acfaf-cc42-4bb7-a830-7226a8007117
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 3%

---


# ZoomViewer{#zoomviewer}

Riferimento API JavaScript per il visualizzatore zoom.

`ZoomViewer([config])`

Crea una nuova istanza del visualizzatore zoom.

## Parametri {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} oggetto di configurazione JSON  </span> facoltativo, consente a tutte le impostazioni del visualizzatore di passare al costruttore per evitare di chiamare i singoli metodi setter. Contiene le seguenti proprietà: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID del contenitore DOM (in genere un  <span class="codeph"> DIV  </span>) in cui viene inserito il visualizzatore. Quando viene chiamato questo metodo, non è necessario creare l'elemento contenitore. Tuttavia, il contenitore deve esistere quando si esegue <span class="codeph"> init() </span>. Obbligatorio. </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <span class="codeph"> params  </span> - Oggetto  <span class="codeph"> {Object}  </span> JSON con parametri di configurazione del visualizzatore in cui il nome della proprietà è un'opzione di configurazione specifica per il visualizzatore o un modificatore SDK, e il valore di tale proprietà è un valore di impostazioni corrispondente. Obbligatorio. </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <span class="codeph"> gestori  </span> - oggetto  <span class="codeph"> {Object}  </span> JSON con callback di eventi del visualizzatore, dove il nome della proprietà è il nome dell'evento del visualizzatore supportato e il valore della proprietà è un riferimento alla funzione JavaScript per il callback appropriato. Facoltativo. <p>Per ulteriori informazioni sugli eventi dei visualizzatori, consultate <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> callback di eventi </a>. </p> </li> 
      <li id="li_1D181A6B1D434B29B09AFD3F4BE059BD"> <span class="codeph"> oggetto JSON localizzatoText  </span> -  <span class="codeph"> {Object}  </span> con dati di localizzazione. Facoltativo. <p>Per ulteriori informazioni, vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localizzazione degli elementi dell'interfaccia utente </a>. </p> <p>Per ulteriori informazioni sul contenuto dell'oggetto, consultate anche la <i>Guida utente dell'SDK per visualizzatori</i>. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"CloseButton.TOOLTIP":"Close" 
}, 
"fr":{ 
"CloseButton.TOOLTIP":"Fermer" 
}, 
defaultLocale:"en" 
} 
});
```

