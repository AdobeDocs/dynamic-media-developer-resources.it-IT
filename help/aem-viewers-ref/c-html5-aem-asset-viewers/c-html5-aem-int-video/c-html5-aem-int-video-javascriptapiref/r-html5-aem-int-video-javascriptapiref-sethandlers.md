---
description: Riferimento API JavaScript per il visualizzatore video interattivo
seo-description: Riferimento API JavaScript per il visualizzatore video interattivo
seo-title: setHandlers
solution: Experience Manager
title: setHandlers
topic: Dynamic media
uuid: f33df5a9-e323-4dff-b792-88d778332c75
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# setHandlers{#sethandlers}

Riferimento API JavaScript per il visualizzatore video interattivo

`setHandlers(handlers)`

Specifica zero o più gestori di callback. Una chiamata a questo metodo sovrascrive completamente i gestori eventi precedentemente assegnati per l’istanza del visualizzatore. Deve essere chiamato prima `init()`.

## Parametro {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestori </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Oggetto {Object} </span> JSON con callback di eventi del visualizzatore, dove il nome della proprietà è il nome dell'evento del visualizzatore supportato e il valore della proprietà è un riferimento alla funzione JavaScript a un callback appropriato. </p> <p>Consultate <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> Callback di eventi </a> per ulteriori informazioni sugli eventi dei visualizzatori. </p> </td> 
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

