---
description: Riferimento API JavaScript per il visualizzatore video.
seo-description: Riferimento API JavaScript per il visualizzatore video.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: ab078f32-c523-4b6c-a0d6-45dd2af35b36
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# setAsset{#setasset}

Riferimento API JavaScript per il visualizzatore video.

[!DNL ` setAsset( *`asset`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> risorsa </span></span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> String </span>} nuovo ID risorsa o set di immagini esplicito con modificatori Image Server facoltativi aggiunti dopo <span class="codeph"> ? </span>. </p> <p> Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta una nuova risorsa. Potete chiamare questo parametro in qualsiasi momento, prima o dopo [!DNL `init()`]. Se viene richiamata, [!DNL `init()`]il visualizzatore scambia la risorsa in fase di esecuzione.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Singolo riferimento a un set di immagini definito in un catalogo:

```
 <instance>.setAsset("Viewers/Pluralist")
```

Set di immagini esplicito, con pagine precombinate:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

Set di immagini esplicito, con immagini di singole pagine:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

Modificatore nitidezza aggiunto a tutte le immagini del set:

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```

