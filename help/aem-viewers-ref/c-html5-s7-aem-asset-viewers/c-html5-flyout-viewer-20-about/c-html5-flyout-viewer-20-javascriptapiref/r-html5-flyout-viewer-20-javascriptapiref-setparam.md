---
description: Riferimento API JavaScript per il visualizzatore a comparsa.
seo-description: Riferimento API JavaScript per il visualizzatore a comparsa.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: 0c2deb6c-f40f-47e5-a1ef-f5eb5db6ee06
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---


# setParam{#setparam}

Riferimento API JavaScript per il visualizzatore a comparsa.

` setParam( *`name, value`*)`

Imposta il parametro del visualizzatore su un valore specificato. Il parametro può essere un’opzione di configurazione specifica per il visualizzatore o un modificatore del kit di sviluppo software. Questo parametro viene chiamato prima di `init()`. Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono trasmesse con l&#39;oggetto JSON `config` al costruttore.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> name del parametro. </p> </td> 
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

