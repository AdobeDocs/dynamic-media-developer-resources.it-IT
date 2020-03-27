---
description: Riferimento API JavaScript per il visualizzatore Video360.
seo-description: Riferimento API JavaScript per il visualizzatore Video360.
seo-title: Video360Viewer
solution: Experience Manager
title: Video360Viewer
topic: Dynamic media
uuid: b5d5e270-687c-40aa-9de4-c5bc2a7806f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360Viewer{#video-viewer}

Riferimento API JavaScript per il visualizzatore Video360.

`Video360Viewer([config])`

Crea una nuova istanza di visualizzatore HTML5 Video360.

## Parametri {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> config </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> oggetto di configurazione JSON facoltativo. Consente a tutte le impostazioni del visualizzatore di passare al costruttore per evitare di chiamare i singoli metodi setter. Contiene le seguenti proprietà: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> <span class="codeph"> containerId </span> - <span class="codeph"> {String} </span> ID del contenitore DOM (in genere un <span class="codeph"> DIV </span>) in cui viene inserito il visualizzatore. Quando viene chiamato questo metodo, non è necessario creare l'elemento contenitore. Tuttavia, il contenitore deve esistere quando <span class="codeph"> init() </span> viene eseguito. </p> <p>Obbligatorio. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> params </span> - <span class="codeph"> oggetto JSON {Object} </span> con parametri di configurazione del visualizzatore in cui il nome della proprietà è un'opzione di configurazione specifica per il visualizzatore o un modificatore SDK, e il valore di tale proprietà è un valore di impostazioni corrispondente. </p> <p>Obbligatorio. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> gestori </span> - <span class="codeph"> oggetto JSON {Object} </span> con callback di eventi del visualizzatore, dove il nome della proprietà è il nome dell'evento del visualizzatore supportato e il valore della proprietà è un riferimento alla funzione JavaScript per il callback appropriato. </p> <p>Facoltativo. </p> <p>Consultate <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Callback di eventi </a> per ulteriori informazioni sugli eventi dei visualizzatori. </p> </li> 
      <li id="li_42A3F3BEF1004E069F0FB2AE0A30B093"> <p> <span class="codeph"> localizedText </span> - <span class="codeph"> oggetto JSON {Object} </span> con dati di localizzazione. Facoltativo. </p> <p>Per ulteriori informazioni, consulta <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1" format="dita" scope="local"> Localizzazione degli elementi dell’interfaccia utente </a> . </p> <p>Per ulteriori informazioni sul contenuto dell’oggetto, consultate anche la Guida <i>utente dell’SDK per</i> visualizzatori e l’esempio. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
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

