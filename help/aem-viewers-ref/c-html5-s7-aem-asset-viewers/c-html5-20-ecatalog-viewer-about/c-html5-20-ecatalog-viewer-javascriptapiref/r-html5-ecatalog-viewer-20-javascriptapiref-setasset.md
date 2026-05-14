---
title: setAsset
description: Guida di riferimento dell’API JavaScript per il visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 04b6bf4d-5c42-49e9-b585-de75ebf6c89f
TQID: 'https://experienceleague.adobe.com/vvkUPbunwRcV80Q7SNvUGaA-LAatPhxASa6y1wOz0eg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 0%

---

# setAsset{#setasset}

Guida di riferimento dell’API JavaScript per il visualizzatore video.

` setAsset( *`risorsa`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> risorsa </span> </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Stringa </span>} ID nuova risorsa o set di immagini esplicito con modificatori Image Server opzionali aggiunti dopo <span class="codeph"> ? </span>. </p> <p> Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta una nuova risorsa. È possibile chiamare questo parametro in qualsiasi momento, prima o dopo `init()`. Se viene chiamato dopo `init()`, il visualizzatore scambia la risorsa in fase di runtime.

Vedi anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Riferimento singolo a un set di immagini definito in un catalogo:

```
 <instance>.setAsset("Viewers/Pluralist")
```

Set di immagini esplicito, con pagine pre-combinate:

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C,Scene7SharedAssets/Backpack_H,Scene7SharedAssets/Backpack_J")
```

Set di immagini esplicito, con singole immagini della pagina:

```
 <instance>.setAsset("Scene7SharedAssets/AdobeScene7_Overview_US-1,Scene7SharedAssets/AdobeScene7_Overview_US-2:AdobeScene7_Overview_US-3,Scene7SharedAssets/AdobeScene7_Overview_US-4")
```

Modificatore di nitidezza aggiunto a tutte le immagini del set:

```
 <instance>.setAsset("Viewers/Pluralist?op_sharpen=1")
```
