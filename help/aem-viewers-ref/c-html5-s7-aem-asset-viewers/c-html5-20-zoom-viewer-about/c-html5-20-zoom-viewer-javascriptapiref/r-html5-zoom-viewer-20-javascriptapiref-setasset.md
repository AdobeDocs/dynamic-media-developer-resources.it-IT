---
description: Riferimento API JavaScript per il visualizzatore video.
seo-description: Riferimento API JavaScript per il visualizzatore video.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: f106b3d4-880e-4ba3-ae47-a005af5c0f1b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

Riferimento API JavaScript per il visualizzatore video.

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> risorsa </span></span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} nuovo ID risorsa, set di immagini esplicito o set di immagini esplicito con modificatori Image Server specifici per ciascun fotogramma, con i modificatori Image Server globali facoltativi aggiunti dopo "?". </p> <p> Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta la nuova risorsa. Potete chiamare questo parametro in qualsiasi momento, prima o dopo `init()`. Se viene richiamata, `init()`il visualizzatore scambia la risorsa in fase di esecuzione.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Riferimento immagine singolo:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Singolo riferimento a un set di immagini definito in un catalogo:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Set di immagini esplicito:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Set di immagini esplicito con modificatori Image Serving specifici per un fotogramma:

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Modificatore nitidezza aggiunto a tutte le immagini del set:

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```

