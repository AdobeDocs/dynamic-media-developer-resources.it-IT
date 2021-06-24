---
description: Riferimento API JavaScript per visualizzatori di file multimediali diversi.
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: 610a5a7d-1314-48bc-a640-319139d64adc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---

# setParam{#setparam}

Riferimento API JavaScript per visualizzatori di file multimediali diversi.

` setParam( *`nome, valore`*)`

Imposta il parametro del visualizzatore su un valore specificato. Il parametro è un&#39;opzione di configurazione specifica per il visualizzatore o un modificatore del kit di sviluppo software. Questo parametro viene chiamato prima di `init()`. Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono passate con l’oggetto JSON `config` al costruttore.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> nome del parametro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> valore del parametro. Il valore non può essere codificato in percentuale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
