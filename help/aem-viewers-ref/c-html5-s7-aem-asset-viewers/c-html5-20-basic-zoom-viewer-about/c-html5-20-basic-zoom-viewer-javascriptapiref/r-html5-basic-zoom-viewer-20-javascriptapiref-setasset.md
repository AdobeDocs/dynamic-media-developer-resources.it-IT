---
description: Riferimento API JavaScript per visualizzatore zoom di base.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---


# setAsset{#setasset}

Riferimento API JavaScript per visualizzatore zoom di base.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> risorsa</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} nuovo ID risorsa, con i modificatori IS facoltativi aggiunti dopo "?" </p> <p> Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta la nuova risorsa. Puoi chiamare questo parametro in qualsiasi momento, prima o dopo `init()`. Se viene chiamato dopo `init()`, il visualizzatore scambia la risorsa in fase di runtime.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Riferimento immagine singolo:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Modificatore di nitidezza aggiunto a tutte le immagini del set:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```

