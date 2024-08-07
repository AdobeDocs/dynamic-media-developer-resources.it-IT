---
title: setAsset
description: Riferimento API di JavaScript per il visualizzatore di file multimediali diversi.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3ad78de9-17a6-40c9-b389-a1f7eed11635
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# setAsset{#setasset}

Riferimento API di JavaScript per il visualizzatore di file multimediali diversi.

` setAsset( *`risorsa`*[,data]))`

Imposta la nuova risorsa e dati facoltativi aggiuntivi sulla risorsa. È possibile chiamare questo parametro in qualsiasi momento, prima o dopo `init()`. Se viene chiamato dopo `init()`, il visualizzatore scambia la risorsa in fase di runtime.

Vedi anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Parametri {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`risorsa`*` - { `String`} nuovo ID risorsa o set di file multimediali diversi esplicito, con modificatori Image Server facoltativi aggiunti dopo `?`.

Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

`*`dati`*` - posizione { `JSON`} del nuovo file di didascalia.

Se non viene specificato, il pulsante della didascalia non è visibile nell&#39;interfaccia utente. I sottotitoli specificati con questo parametro si applicano al video che arriva primo nel set di file multimediali diversi; i video successivi vengono riprodotti senza sottotitoli. Questo visualizzatore supporta i seguenti ID componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nome classe componente SDK per visualizzatore </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine posteriore </span> </p> </td> 
   <td colname="col2"> <p>Immagine da visualizzare sul primo fotogramma prima che inizi la riproduzione del video. </p> <p>Vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> didascalia </span> </p> </td> 
   <td colname="col2"> <p> Posizione del nuovo file di didascalia. </p> <p>Se non viene specificato, il pulsante della didascalia non è visibile nell'interfaccia utente. I sottotitoli specificati con questo parametro si applicano al video che arriva primo nel set di file multimediali. I video successivi vengono riprodotti senza didascalie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Riferimento a un singolo set di file multimediali:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

Set di file multimediali esplicito:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

Modificatore di nitidezza aggiunto a tutte le immagini del set:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```
