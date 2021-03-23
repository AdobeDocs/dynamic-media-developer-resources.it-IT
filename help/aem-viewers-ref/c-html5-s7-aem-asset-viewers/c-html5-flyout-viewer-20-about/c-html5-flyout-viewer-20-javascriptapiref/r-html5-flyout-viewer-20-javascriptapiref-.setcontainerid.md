---
description: Riferimento API JavaScript per il visualizzatore a comparsa.
seo-description: Riferimento API JavaScript per il visualizzatore a comparsa.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
uuid: 9a124dfb-e094-4426-8c46-aa1a784b127d
feature: Dynamic Media Classic,Visualizzatori,SDK/API,A comparsa
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# setContainerId{#setcontainerid}

Riferimento API JavaScript per il visualizzatore a comparsa.

` setContainerId( *`containerId`*)`

Imposta l’ID del contenitore DOM (di solito un `DIV`) in cui viene inserito il visualizzatore. Non è necessario che l&#39;elemento contenitore venga creato al momento della chiamata di questo metodo. Tuttavia, il contenitore deve esistere quando viene eseguito `init()`. Deve essere chiamato prima di `init()`. Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono passate con l’oggetto JSON `config` al costruttore.

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

