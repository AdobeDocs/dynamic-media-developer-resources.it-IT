---
title: setHandlers
description: Riferimento API di JavaScript per il visualizzatore 360 gradi
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: f9e0b93e-fb27-4530-93cf-8246948423d9
TQID: 'https://experienceleague.adobe.com/qBKG0owQBEJ77UvS4oZ4lOzqkg-Z5Kgf2kImZbFxmCU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 1%

---

# setHandlers{#sethandlers}

Riferimento API di JavaScript per il visualizzatore 360 gradi

`setHandlers(handlers)`

Specifica zero o più gestori di callback. Una chiamata a questo metodo sovrascrive completamente i gestori eventi precedentemente assegnati per tale istanza del visualizzatore. Deve essere chiamato prima di `init()`.

## Parametro {#section-51f820ded5e842bebd123e37a35176c7}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> gestori </span> </span> </p> </td> 
   <td colname="col2"> <p> Oggetto JSON <span class="codeph"> {Object} </span> con callback di eventi del visualizzatore, in cui il nome della proprietà è il nome dell'evento del visualizzatore supportato e il valore della proprietà è un riferimento di funzione JavaScript a un callback appropriato. </p> <p>Per ulteriori informazioni sugli eventi visualizzatore, vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-event-callbacks.md#concept-9c553c80eefd422faacf6522c69804bf" format="dita" scope="local"> callback di eventi </a>. </p> </td> 
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
