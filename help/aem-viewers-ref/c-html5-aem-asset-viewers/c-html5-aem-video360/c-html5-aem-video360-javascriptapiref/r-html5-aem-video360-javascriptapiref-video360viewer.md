---
title: Visualizzatore video360i
description: Riferimento API di JavaScript per il visualizzatore Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: ab22ff22-45a7-490e-932d-7c885ff5c3a9
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 2%

---

# Visualizzatore video360i{#video-viewer}

Riferimento API di JavaScript per il visualizzatore Video360.

`Video360Viewer([config])`

Costruttore, crea una nuova istanza di HTML5 Video360 Viewer.

## Parametri {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configurazione </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> oggetto di configurazione JSON facoltativo, consente a tutte le impostazioni del visualizzatore di passare al costruttore per evitare di chiamare singoli metodi di impostazione. Contiene le seguenti proprietà: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> ID <span class="codeph"> contenitore </span> - ID <span class="codeph"> {String} </span> del contenitore DOM (normalmente un DIV <span class="codeph"> </span>) in cui è inserito il visualizzatore. Quando si chiama questo metodo, non è necessario creare l’elemento contenitore. Tuttavia, il contenitore deve esistere quando viene eseguito <span class="codeph"> init() </span>. </p> <p>Obbligatorio. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> parametri </span> - <span class="codeph"> {Object} </span> oggetto JSON con parametri di configurazione del visualizzatore in cui il nome della proprietà è un'opzione di configurazione specifica del visualizzatore o un modificatore SDK e il valore di tale proprietà è un valore di impostazioni corrispondente. </p> <p>Obbligatorio. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> gestori </span> - <span class="codeph"> {Object} </span> oggetto JSON con callback di eventi visualizzatore, in cui il nome della proprietà è il nome dell'evento visualizzatore supportato e il valore della proprietà è un riferimento di funzione JavaScript al callback appropriato. </p> <p>Facoltativo. </p> <p>Per ulteriori informazioni sugli eventi visualizzatore, vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> callback di eventi </a>. </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> <span class="codeph"> localizedTexts </span> - <span class="codeph"> {Object} </span> oggetto JSON con dati di localizzazione. Facoltativo. </p> <p>Per ulteriori informazioni, vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> Localizzazione degli elementi dell'interfaccia utente </a>. </p> <p>Per ulteriori informazioni sul contenuto dell'oggetto, vedere anche la <i>Guida utente di Viewer SDK</i> e l'esempio. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.


## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played." 
}, 
"fr":{ 
"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus." 
}, 
defaultLocale:"en" 
} 
});
```

