---
title: setHandlers
description: Riferimento API JavaScript per i visualizzatori zoom di base
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: d800dbbc-2c40-4911-8f29-c8413847f7be
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# setHandlers{#sethandlers}

Riferimento API JavaScript per i visualizzatori zoom di base

`setHandlers(handlers)`

Specifica zero o più gestori di callback. Una chiamata a questo metodo sovrascrive completamente i gestori eventi precedentemente assegnati per l&#39;istanza di visualizzatore. Deve essere chiamato prima `init()`.

## Parametro {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestori </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {Object} </span> Oggetto JSON con callback di eventi del visualizzatore, in cui il nome della proprietà è il nome dell’evento del visualizzatore supportato e il valore della proprietà è un riferimento alla funzione JavaScript per un callback appropriato. </p> <p>Vedi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-event-callbacks.md#concept-8ba57cf86537401999514e1b221ec734" format="dita" scope="local"> Callback degli eventi </a> per ulteriori informazioni sugli eventi del visualizzatore. </p> </td> 
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
