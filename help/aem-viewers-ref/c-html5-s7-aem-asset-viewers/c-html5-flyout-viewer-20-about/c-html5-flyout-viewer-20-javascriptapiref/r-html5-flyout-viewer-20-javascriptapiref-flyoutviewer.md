---
title: Visualizzatore a comparsa
description: Riferimento API di JavaScript per il visualizzatore a comparsa.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b64f16c8-03bf-4603-972f-845a4c1e2b02
source-git-commit: f970421ccc482b698343aa18e7dfde7bea4c2a89
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 2%

---

# Visualizzatore a comparsa{#flyoutviewer}

Riferimento API di JavaScript per il visualizzatore a comparsa.

`FlyoutViewer([config])`

Costruttore; crea un&#39;istanza del visualizzatore a comparsa.

## Parametri {#section-8bc3d1424c8444f193716fc8d9975765}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configurazione </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> oggetto di configurazione JSON facoltativo, consente a tutte le impostazioni del visualizzatore di passare al costruttore ed evitare di chiamare i singoli metodi di impostazione. Contiene le seguenti proprietà: </p> <p> 
     <ul id="ul_266C711E8E75471E90C15F39A96A142F"> 
      <li id="li_71857BBD652243A094E936C2C8EA9702"> ID <span class="codeph"> contenitore </span> - ID <span class="codeph"> {String} </span> del contenitore DOM (normalmente un DIV <span class="codeph"> di </span>) in cui è inserito il visualizzatore. Non è necessario creare l’elemento contenitore nel momento in cui viene chiamato questo metodo. Tuttavia, il contenitore deve esistere quando viene eseguito <span class="codeph"> init() </span>. Obbligatorio. </li> 
      <li id="li_3D28979F04274AC9B507B33D4275FC3A"> <span class="codeph"> parametri </span> - <span class="codeph"> {Object} </span> oggetto JSON con parametri di configurazione del visualizzatore in cui il nome della proprietà è un'opzione di configurazione specifica del visualizzatore o un modificatore SDK e il valore di tale proprietà è un valore di impostazioni corrispondente. Obbligatorio. </li> 
      <li id="li_A40AC2167575415FB3383D070E27B9AB"> <span class="codeph"> gestori </span> - <span class="codeph"> {Object} </span> oggetto JSON con callback di eventi visualizzatore, in cui il nome della proprietà è il nome dell'evento visualizzatore supportato e il valore della proprietà è un riferimento di funzione JavaScript a un callback appropriato. Facoltativo. <p>Per ulteriori informazioni sugli eventi visualizzatore, vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> callback di eventi </a>. </p> </li> 
      <li id="li_218F9597A60249AEBA43A9E86EAFF8BA"> <p> <span class="codeph"> localizedTexts </span> - { <span class="codeph"> Oggetto </span>} oggetto JSON con dati di localizzazione. Facoltativo. </p> <p>Per ulteriori informazioni, vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27" format="dita" scope="local"> Localizzazione degli elementi dell'interfaccia utente </a>. </p> <p>Per ulteriori informazioni sul contenuto dell'oggetto, vedere la <i>Guida utente di Viewer SDK</i> e l'esempio. Facoltativo. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var flyoutViewer = new s7viewers.FlyoutViewer({ 
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
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom" 
}, 
"fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer" 
}, 
defaultLocale:"en" 
} 
});
```
