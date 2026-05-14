---
title: setAsset
description: Riferimento API di JavaScript per il visualizzatore a comparsa.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: cd66267e-7b25-4af4-b83c-f7b7f768ea8c
TQID: 'https://experienceleague.adobe.com/4y4sUkQ-29q5xLQuSmTyLSHj-VSAZ2GNY1qFhQreoJg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 0%

---

# setAsset{#setasset}

Riferimento API di JavaScript per il visualizzatore a comparsa.

` setAsset( *`risorsa`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> risorsa</span> </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> String</span>} ID nuova risorsa, set di immagini esplicito o set di immagini esplicito con modificatori Image Server specifici per frame, con modificatori Image Server globali facoltativi aggiunti dopo <span class="codeph"> ?</span>. </p> <p> Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore. </p> </td> 
  </tr> 
 </tbody> 
</table>

Imposta la nuova risorsa. È possibile chiamare questo parametro in qualsiasi momento, prima o dopo `init()`. Se viene chiamato dopo `init()`, il visualizzatore scambia la risorsa in fase di runtime.

Vedi anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-init.md#reference-8651640683fc4a538bfb660709d1a463).

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Riferimento a immagine singola:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

Riferimento singolo a un set di immagini definito in un catalogo:

```
<instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

Immagine esplicita impostata come segue:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

Set di immagini esplicito con modificatori Image Server specifici per frame:

```
<instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

Modificatore di nitidezza aggiunto a tutte le immagini del set:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C?op_sharpen=1")
```
