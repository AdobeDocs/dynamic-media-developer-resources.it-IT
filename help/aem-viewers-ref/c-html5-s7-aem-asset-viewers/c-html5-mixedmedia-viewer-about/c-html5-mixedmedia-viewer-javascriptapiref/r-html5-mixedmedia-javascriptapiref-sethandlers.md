---
title: setHandlers
description: Riferimento API JavaScript per visualizzatori di file multimediali diversi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e30f1b73-1dba-4d4c-9e90-f343ca404550
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# setHandlers{#sethandlers}

Riferimento API JavaScript per visualizzatori di file multimediali diversi.

`setHandlers(handlers)`

Specifica zero o più gestori di callback. Una chiamata a questo metodo sovrascrive completamente i gestori eventi precedentemente assegnati per l&#39;istanza di visualizzatore. Deve essere chiamato prima `init()`.

## Parametro {#section-0cc9961784d04eb3b7d50011309b0119}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestori </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> Oggetto JSON con callback di eventi del visualizzatore, in cui il nome della proprietà è il nome dell’evento del visualizzatore supportato e il valore della proprietà è un riferimento alla funzione JavaScript per un callback appropriato. </p> <p>Vedi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-event-callbacks.md#concept-273d2cddbb7144e284b618ffaf3deabc" format="dita" scope="local"> Callback degli eventi </a> per ulteriori informazioni sugli eventi del visualizzatore. </p> </td> 
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
