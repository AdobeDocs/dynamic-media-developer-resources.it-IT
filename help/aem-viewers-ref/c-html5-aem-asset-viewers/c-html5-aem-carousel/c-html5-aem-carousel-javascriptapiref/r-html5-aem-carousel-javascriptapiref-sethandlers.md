---
description: Riferimento API JavaScript per il visualizzatore carosello
seo-description: Riferimento API JavaScript per il visualizzatore carosello
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic Media
uuid: 5e1e9c8f-866b-4730-9978-b45face85667
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 3%

---


# setHandlers{#sethandlers}

Riferimento API JavaScript per il visualizzatore carosello

`setHandlers(handlers)`

Specifica zero o più gestori di callback. Una chiamata a questo metodo sovrascrive completamente i gestori eventi precedentemente assegnati per l’istanza del visualizzatore. Deve essere chiamato prima di `init()`.

## Parametro {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> handler  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Oggetto  </span> JSON {Object} con callback di eventi del visualizzatore. Il nome della proprietà è il nome dell'evento di visualizzatore supportato. Il valore della proprietà è un riferimento alla funzione JavaScript per un callback appropriato. </p> <p>Per ulteriori informazioni sugli eventi dei visualizzatori, consultate <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> callback di eventi </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  console.log("init complete"); 
} 
})
```

