---
title: CarouselViewer
description: Riferimento API di JavaScript per il visualizzatore carosello.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 890d869d-dbf2-4c24-88d1-34c439ab1e3a
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# CarouselViewer{#carouselviewer}

Riferimento API di JavaScript per il visualizzatore carosello.

`CarouselViewer([config])`

Costruttore, crea un’istanza del visualizzatore carosello HTML 5.

## Parametri {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configurazione </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {object} </span> oggetto di configurazione JSON facoltativo, consente a tutte le impostazioni del visualizzatore di passare al costruttore per evitare di chiamare singoli metodi di impostazione. Contiene le seguenti proprietà: </p> <p> 
     <ul id="ul_789DBD5B72ED4C80B685455B0D59494D"> 
      <li id="li_28FDCB53E4AD4097A51F21B876C18FB1"> <p> ID <span class="codeph"> contenitore </span> - ID <span class="codeph"> {String} </span> del contenitore DOM (normalmente un DIV <span class="codeph"> di </span>) in cui è inserito il visualizzatore. Quando si chiama questo metodo, non è necessario creare l’elemento contenitore. Tuttavia, il contenitore deve esistere quando viene eseguito <span class="codeph"> init() </span>. </p> <p>Obbligatorio. </p> </li> 
      <li id="li_FDE00392DC1544ABBDD75F81EF814EF2"> <p> <span class="codeph"> parametri </span> - <span class="codeph"> {Object} </span> oggetto JSON con parametri di configurazione del visualizzatore in cui il nome della proprietà è un'opzione di configurazione specifica del visualizzatore o un modificatore SDK e il valore di tale proprietà è un valore di impostazioni corrispondente. </p> <p>Obbligatorio. </p> </li> 
      <li id="li_C534D5091CDA4717BCC48E3EBBF09AB8"> <p> <span class="codeph"> gestori </span> - <span class="codeph"> {Object} </span> oggetto JSON con callback di eventi visualizzatore, in cui il nome della proprietà è il nome dell'evento visualizzatore supportato e il valore della proprietà è un riferimento di funzione JavaScript al callback appropriato. </p> <p>Facoltativo. </p> <p>Per ulteriori informazioni sugli eventi visualizzatore, vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> callback di eventi </a>. </p> </li> 
      <li id="li_CD88EDB586B241DBB87B13709F24C454"> <p> <span class="codeph"> testi localizzati </span> - <span class="codeph"> {Object} </span> </p> <p> Oggetto JSON con dati di localizzazione. Per ulteriori informazioni sul contenuto dell’oggetto, vedi Localizzazione degli elementi dell’interfaccia utente e l’esempio. </p> <p>Facoltativo </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

<!-- ## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3} -->

<!--

```javascript {.line-numbers}
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
}, 
"handlers":{ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
}, 
"localizedTexts":{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left" 
}, 
"fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste" 
}, 
defaultLocale:"en" 
} 
});
```

-->
