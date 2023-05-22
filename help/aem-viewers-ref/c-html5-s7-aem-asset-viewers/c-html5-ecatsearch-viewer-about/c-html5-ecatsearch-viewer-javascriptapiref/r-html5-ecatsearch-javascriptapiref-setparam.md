---
description: Riferimento API JavaScript per il visualizzatore eCatalog.
solution: Experience Manager
title: setParam
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 0dd57c7e-c20f-4e8f-a872-42e24305fc0c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 2%

---

# setParam{#setparam}

Riferimento API JavaScript per il visualizzatore eCatalog.

[!DNL ` setParam( *`nome, valore`*)`]

Imposta il parametro del visualizzatore su un valore specificato. Il parametro può essere un&#39;opzione di configurazione specifica del visualizzatore o un modificatore del kit di sviluppo software. Questo parametro viene chiamato prima di [!DNL `init()`].

Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono trasmesse con [!DNL `config`] Oggetto JSON al costruttore.

Vedi anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

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
[!DNL <instance>.setParam("style", "customStyle.css")]
```
