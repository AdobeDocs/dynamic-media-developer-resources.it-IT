---
title: setHandlers
description: Riferimento API di JavaScript per il visualizzatore carosello
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: d269627a-e2f8-4ca6-96a1-a7dce312e06e
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 1%

---

# setHandlers{#sethandlers}

Riferimento API di JavaScript per il visualizzatore carosello

`setHandlers(handlers)`

Specifica zero o più gestori di callback. Una chiamata a questo metodo sovrascrive completamente i gestori eventi precedentemente assegnati per tale istanza del visualizzatore. Deve essere chiamato prima di `init()`.

## Parametro {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestori </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> oggetto JSON con callback di eventi del visualizzatore. Il nome della proprietà è il nome dell’evento visualizzatore supportato. Il valore della proprietà è un riferimento della funzione JavaScript a un callback appropriato. </p> <p>Per ulteriori informazioni sugli eventi visualizzatore, vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> callback di eventi </a>. </p> </td> 
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
