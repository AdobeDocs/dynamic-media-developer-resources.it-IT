---
description: Riferimento API JavaScript per il visualizzatore a 360 gradi.
solution: Experience Manager
title: SpinViewer
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set 360 gradi
role: Developer,Business Practitioner
exl-id: 0cfde665-c578-41a0-a428-0db3cbdac6ae
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 3%

---

# SpinViewer{#spinviewer}

Riferimento API JavaScript per il visualizzatore a 360 gradi.

`SpinViewer([config])`

Costrutore, crea una nuova istanza del visualizzatore a 360 gradi.

## Parametri {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} oggetto di configurazione JSON  </span> opzionale, consente a tutte le impostazioni del visualizzatore di passare al costruttore ed evitare di chiamare i singoli metodi del setter. Contiene le seguenti proprietà: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <p> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID del contenitore DOM (in genere un  <span class="codeph"> DIV  </span>) in cui viene inserito il visualizzatore. Non è necessario che l'elemento contenitore venga creato al momento della chiamata di questo metodo. Tuttavia, il contenitore deve esistere quando viene eseguito <span class="codeph"> init() </span> . Obbligatorio. </p> </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <p> <span class="codeph"> params  </span> - Oggetto  <span class="codeph"> {Object}  </span> JSON con parametri di configurazione del visualizzatore in cui il nome della proprietà è un'opzione di configurazione specifica per il visualizzatore o un modificatore SDK e il valore di tale proprietà è un valore di impostazioni corrispondente. Obbligatorio. </p> </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <p> <span class="codeph"> gestori  </span> -  <span class="codeph"> {Object} oggetto  </span> JSON con callback di eventi del visualizzatore, dove il nome della proprietà è il nome dell'evento del visualizzatore supportato e il valore della proprietà è un riferimento alla funzione JavaScript a un callback appropriato. Facoltativo. </p> <p>Per ulteriori informazioni sugli eventi del visualizzatore, consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> callback di eventi </a> . </p> </li> 
      <li id="li_643787FB4A424D0AB6B8E12F44C3A9AC"> <p> <span class="codeph"> oggetto  </span> JSON localizzatoTesti  <span class="codeph"> -  </span> {Object} con dati di localizzazione. Facoltativo. </p> <p>Per ulteriori informazioni, consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98" format="dita" scope="local"> Localizzazione degli elementi dell’interfaccia utente </a> . </p> <p>Per ulteriori informazioni sul contenuto dell’oggetto, consulta anche la <i>Guida utente dell’SDK per visualizzatori</i> e l’esempio . </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
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
