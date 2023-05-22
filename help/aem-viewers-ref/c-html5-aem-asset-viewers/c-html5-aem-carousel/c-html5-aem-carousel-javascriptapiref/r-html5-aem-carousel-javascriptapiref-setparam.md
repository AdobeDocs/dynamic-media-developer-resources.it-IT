---
title: setParam
description: Riferimento API JavaScript per il visualizzatore carosello.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 0829933f-a90b-4066-9904-748f2a727169
source-git-commit: 96ac67e5645c2c55920cc971806ba2f14ae57044
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 2%

---

# setParam{#setparam}

Riferimento API JavaScript per il visualizzatore carosello.

` setParam( *`nome, valore`*)`

Imposta il parametro del visualizzatore su un valore specificato. Il parametro può essere un&#39;opzione di configurazione specifica del visualizzatore o un modificatore del kit di sviluppo software. Questo parametro viene chiamato prima di `init()`.

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore sono state trasmesse con `config` Oggetto JSON per il costruttore.

Vedi anche [xref](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-init.md).

## Parametri {#section-c68a5a3688d342fd9d6a7fd59867cc7a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> nome </span> </span> </p> </td>
   <td colname="col2"> <p> <span class="codeph"> {string} </span> nome del parametro. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> valore </span> </span> </p> </td>
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
