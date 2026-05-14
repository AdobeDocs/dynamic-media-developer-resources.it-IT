---
title: setHandlers
description: Riferimento API di JavaScript per il visualizzatore video
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: cff331a9-bca1-4360-88fa-96812aa8ba62
TQID: 'https://experienceleague.adobe.com/YH8rHZduymKOkXHF1tBAwb1ramR8yIgmVXRl904eVxY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 1%

---

# setHandlers{#sethandlers}

Riferimento API di JavaScript per il visualizzatore video

`setHandlers(handlers)`

Specifica zero o più gestori di callback. Una chiamata a questo metodo sovrascrive completamente i gestori eventi precedentemente assegnati per tale istanza del visualizzatore. Deve essere chiamato prima di `init()`.

## Parametro {#section-b60f082cca1542748b605689b1d43f8a}

<table id="table_98A620DAE2C340FA97BF7204AE023CC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestori </span> </span> </p> </td> 
   <td colname="col2"> <p> Oggetto JSON <span class="codeph"> {Object} </span> con callback di eventi del visualizzatore, in cui il nome della proprietà è il nome dell'evento del visualizzatore supportato e il valore della proprietà è un riferimento di funzione JavaScript a un callback appropriato. </p> <p>Per ulteriori informazioni sugli eventi visualizzatore, vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-event-callbacks.md#concept-66d5996f2b1b44cab3d5264cda5c50cd" format="dita" scope="local"> callback di eventi </a>. </p> </td> 
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
