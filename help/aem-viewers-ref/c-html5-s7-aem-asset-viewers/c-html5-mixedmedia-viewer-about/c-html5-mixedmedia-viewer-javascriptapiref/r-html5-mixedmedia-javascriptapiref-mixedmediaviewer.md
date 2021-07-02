---
description: Riferimento API JavaScript per visualizzatori di file multimediali diversi.
solution: Experience Manager
title: MixedMediaViewer
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: b7f09f51-409e-4dfa-9041-b82767d4e35f
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---

# MixedMediaViewer{#mixedmediaviewer}

Riferimento API JavaScript per visualizzatori di file multimediali diversi.

`MixedMediaViewer([config])`

Crea una nuova istanza del visualizzatore di file multimediali diversi.

## Parametri {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} oggetto di configurazione JSON  </span> opzionale, consente a tutte le impostazioni del visualizzatore di passare al costruttore ed evitare di chiamare i singoli metodi del setter. Contiene le seguenti proprietà: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> <span class="codeph"> containerId  </span> -  <span class="codeph"> {String}  </span> ID del contenitore DOM (in genere un  <span class="codeph"> DIV  </span>) in cui viene inserito il visualizzatore. Non è necessario che l'elemento contenitore venga creato al momento della chiamata di questo metodo. Tuttavia, il contenitore deve esistere quando viene eseguito <span class="codeph"> init() </span> . Obbligatorio. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> params  </span> - Oggetto  <span class="codeph"> {Object}  </span> JSON con parametri di configurazione del visualizzatore in cui il nome della proprietà è un'opzione di configurazione specifica per il visualizzatore o un modificatore SDK e il valore di tale proprietà è un valore di impostazioni corrispondente. Obbligatorio. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> gestori  </span> -  <span class="codeph"> {Object} oggetto  </span> JSON con callback di eventi del visualizzatore, dove il nome della proprietà è il nome dell'evento del visualizzatore supportato e il valore della proprietà è un riferimento alla funzione JavaScript a un callback appropriato. Facoltativo. <p>Per ulteriori informazioni sugli eventi del visualizzatore, consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-event-callbacks.md#concept-273d2cddbb7144e284b618ffaf3deabc" format="dita" scope="local"> callback di eventi </a> . </p> </li> 
      <li id="li_C592026403804A4FAE12863944A10EE4"> <p> <span class="codeph"> localizedText  </span> - {  <span class="codeph"> Object  </span>} oggetto JSON con dati di localizzazione. Facoltativo. </p> <p>Per ulteriori informazioni, consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> Localizzazione degli elementi dell’interfaccia utente </a> . </p> <p>Per ulteriori informazioni sul contenuto dell’oggetto, consulta anche la <i>Guida utente dell’SDK per visualizzatori</i> e l’esempio . </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
