---
description: Riferimento API JavaScript per il visualizzatore zoom di base.
seo-description: Riferimento API JavaScript per il visualizzatore zoom di base.
seo-title: BasicZoomViewer
solution: Experience Manager
title: BasicZoomViewer
topic: Dynamic media
uuid: 727e38af-636a-4eb3-b373-6940169d006b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# BasicZoomViewer{#basiczoomviewer}

Riferimento API JavaScript per il visualizzatore zoom di base.

`BasicZoomViewer([config])`

Crea una nuova istanza del visualizzatore zoom di base.

## Parametri {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> oggetto di configurazione JSON facoltativo. Consente a tutte le impostazioni del visualizzatore di passare al costruttore per evitare di chiamare i singoli metodi setter. Contiene le seguenti proprietà: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID del contenitore DOM (in genere un <span class="codeph"> DIV </span>) in cui viene inserito il visualizzatore. Quando viene chiamato questo metodo, non è necessario creare l'elemento contenitore. Tuttavia, il contenitore deve esistere quando <span class="codeph"> init() </span> viene eseguito. Obbligatorio. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> oggetto JSON {Object} </span> con parametri di configurazione del visualizzatore in cui il nome della proprietà è un'opzione di configurazione specifica per il visualizzatore o un modificatore SDK, e il valore di tale proprietà è un valore di impostazioni corrispondente. Obbligatorio. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> gestori </span> - <span class="codeph"> oggetto JSON {Object} </span> con callback di eventi del visualizzatore, dove il nome della proprietà è il nome dell'evento del visualizzatore supportato e il valore della proprietà è un riferimento alla funzione JavaScript per il callback appropriato. Facoltativo. </p> <p>Consultate <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-event-callbacks.md#concept-8ba57cf86537401999514e1b221ec734" format="dita" scope="local"> Callback di eventi </a> per ulteriori informazioni sugli eventi dei visualizzatori. </p> </li> 
      <li id="li_528FE03845F847E08F964E38D6AB6E86"> <p> <span class="codeph"> localizedText </span> - <span class="codeph"> oggetto JSON {Object} </span> con dati di localizzazione. Facoltativo. </p> <p>Per ulteriori informazioni, consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74" format="dita" scope="local"> Localizzazione degli elementi dell’interfaccia utente </a> . </p> <p> Per ulteriori informazioni sul contenuto dell’oggetto, consultate anche la Guida <i>utente dell’SDK per</i> visualizzatori e l’esempio. Facoltativo </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
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

