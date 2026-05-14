---
title: setParam
description: Riferimento API di JavaScript per il visualizzatore 360 gradi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 16d1d2cd-f58f-4ac3-b89f-f2f12fee231d
TQID: 'https://experienceleague.adobe.com/R0HdN4vDg-LC6em1E3KdzQI5d4uwttBhK1sQPI77Dw8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 1%

---

# setParam{#setparam}

Riferimento API di JavaScript per il visualizzatore 360 gradi.

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

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono passate con l&#39;oggetto JSON `config` al costruttore.

Vedi anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setParam("style", "customStyle.css")
```
