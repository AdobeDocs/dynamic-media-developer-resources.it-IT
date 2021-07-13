---
description: Riferimento API JavaScript per il visualizzatore a comparsa.
solution: Experience Manager
title: setHandlers
feature: Dynamic Media Classic,Visualizzatori,SDK/API,A comparsa
role: Developer,User
exl-id: 3a7b2aeb-2de5-4d4c-8974-47b6418140e6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 3%

---

# setHandlers{#sethandlers}

Riferimento API JavaScript per il visualizzatore a comparsa.

`setHandlers(handlers)`

Specifica zero o più gestori di callback. Una chiamata a questo metodo sovrascrive completamente i gestori eventi precedentemente assegnati per l&#39;istanza di visualizzatore. Deve essere chiamato prima di `init()`.

## Parametro {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestori  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Oggetto  </span> JSON {Object} con callback di eventi del visualizzatore, in cui il nome della proprietà è il nome dell'evento del visualizzatore supportato e il valore della proprietà è un riferimento alla funzione JavaScript a un callback appropriato. </p> <p>Per ulteriori informazioni sugli eventi del visualizzatore, consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-event-callbacks.md#concept-53eb01d28189437790268da4929f2a10" format="dita" scope="local"> callback di eventi </a> . </p> </td> 
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
