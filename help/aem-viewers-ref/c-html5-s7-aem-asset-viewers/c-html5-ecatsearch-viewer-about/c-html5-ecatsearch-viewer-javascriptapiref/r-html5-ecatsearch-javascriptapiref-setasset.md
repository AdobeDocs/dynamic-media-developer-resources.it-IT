---
description: Riferimento API JavaScript per il visualizzatore video.
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Ricerca eCatalog
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---


# setAsset{#setasset}

Riferimento API JavaScript per il visualizzatore video.

[!DNL ` setAsset( *`asset`*)`]

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> risorsa  </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Stringa </span>} nuovo ID risorsa o set di immagini esplicite con modificatori opzionali Image Server aggiunti dopo <span class="codeph"> ? </span>. </p> <p> Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta una nuova risorsa. Puoi chiamare questo parametro in qualsiasi momento, prima o dopo [!DNL `init()`]. Se viene chiamato dopo [!DNL `init()`], il visualizzatore scambia la risorsa in fase di runtime.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Riferimento singolo a un set di immagini definito in un catalogo:

```
 <instance>.setAsset("Viewers/Pluralist")
```

Set di immagini esplicito, con pagine precombinate:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

Set di immagini esplicito, con immagini a pagina singola:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

Modificatore di nitidezza aggiunto a tutte le immagini del set:

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```

