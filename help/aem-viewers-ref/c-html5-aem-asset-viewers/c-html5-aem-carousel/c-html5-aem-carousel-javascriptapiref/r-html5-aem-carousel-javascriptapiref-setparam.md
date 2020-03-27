---
description: Riferimento API JavaScript per il visualizzatore carosello.
seo-description: Riferimento API JavaScript per il visualizzatore carosello.
seo-title: setParam
solution: Experience Manager
title: setParam
topic: Dynamic media
uuid: 87f16ea9-0267-4114-9aeb-a68fdb616a88
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setParam{#setparam}

Riferimento API JavaScript per il visualizzatore carosello.

` setParam( *`name, value`*)`

Imposta il parametro del visualizzatore su un valore specificato. Il parametro può essere un’opzione di configurazione specifica per il visualizzatore o un modificatore del kit di sviluppo software. Questo parametro viene chiamato prima `init()`.

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore sono state trasmesse con l&#39;oggetto `config` JSON al costruttore.

Vedere anche [xref](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md).

## Parametri {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> name </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> nome del parametro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> valore del parametro. Il valore non può essere codificato in percentuale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "etc/dam/presets/css/html5_carouselviewer_dotted_light.css")
```

