---
title: setParam
description: Guida di riferimento dell’API JavaScript per il visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: d797a8be-582e-46f4-9068-db1d2757970d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 1%

---

# setParam{#setparam}

Guida di riferimento dell’API JavaScript per il visualizzatore video.

` setParam( *`nome, valore`*)`

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

Imposta il parametro del visualizzatore su un valore specificato. Il parametro può essere un&#39;opzione di configurazione specifica del visualizzatore o un modificatore del kit di sviluppo software. Questo parametro viene chiamato prima di `init()`.

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore sono state passate con `config` oggetto JSON al costruttore.

Vedi anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
