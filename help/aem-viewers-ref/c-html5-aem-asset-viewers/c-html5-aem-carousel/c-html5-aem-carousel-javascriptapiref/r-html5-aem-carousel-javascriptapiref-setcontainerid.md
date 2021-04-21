---
description: Riferimento API JavaScript per il visualizzatore Carosello.
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 32636cf9-3dc7-4299-a7b7-cf803ca36514
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 3%

---

# setContainerId{#setcontainerid}

Riferimento API JavaScript per il visualizzatore Carosello.

` setContainerId( *`containerId`*)`

Imposta l’ID del contenitore DOM (di solito un `DIV`) in cui viene inserito il visualizzatore. Non è necessario che l&#39;elemento contenitore venga creato al momento della chiamata di questo metodo. Tuttavia, il contenitore deve esistere quando viene eseguito `init()`. Deve essere chiamato prima di `init()`.

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono passate con l&#39;oggetto JSON `config` al costruttore.

## Parametro {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> ID del contenitore. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
