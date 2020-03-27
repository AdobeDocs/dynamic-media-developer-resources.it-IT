---
description: Riferimento API JavaScript per il visualizzatore di file multimediali diversi.
seo-description: Riferimento API JavaScript per il visualizzatore di file multimediali diversi.
seo-title: setAsset
solution: Experience Manager
title: setAsset
topic: Dynamic media
uuid: 8c341a8a-25b5-4db9-ad1a-919ded79f2ed
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAsset{#setasset}

Riferimento API JavaScript per il visualizzatore di file multimediali diversi.

` setAsset( *`asset`*[,data]))`

Imposta la nuova risorsa e i dati facoltativi aggiuntivi. Potete chiamare questo parametro in qualsiasi momento, prima o dopo `init()`. Se viene richiamata, `init()`il visualizzatore scambia la risorsa in fase di esecuzione.

Vedere anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-init.md#reference-bb4428c155e541b79797f96e17c068ae).

## Parametri {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

` *`risorsa`*` - { `String`} nuovo ID risorsa o set di file multimediali misto esplicito, con l’aggiunta di modificatori Image Server facoltativi `?`.

Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

` *`data`*` - { `JSON`} posizione del nuovo file di sottotitoli.

Se non viene specificato, il pulsante della didascalia non è visibile nell&#39;interfaccia utente. Le didascalie specificate con questo parametro si applicano al video che compare per primo nel set di file multimediali diversi; i video successivi vengono riprodotti senza didascalie. Questo visualizzatore supporta i seguenti ID componente:

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>ID componente </p> </th> 
   <th colname="col2" class="entry"> <p>Nome classe componente SDK per visualizzatori </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posterimage </span> </p> </td> 
   <td colname="col2"> <p>Immagine da visualizzare sul primo fotogramma prima che inizi la riproduzione del video. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/r-html5-mixedmedia-viewer-config-attrib/r-html5-mixedmedia-viewer-config-attrib-videoplayer-posterimage.md#reference-f424ad0f278b4d14b86ea55e3a73c52b" format="dita" scope="local"> VideoPlayer.posterimage </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> didascalia </span> </p> </td> 
   <td colname="col2"> <p> Posizione del nuovo file di sottotitoli. </p> <p>Se non viene specificato, il pulsante della didascalia non è visibile nell'interfaccia utente. Le didascalie specificate con questo parametro si applicano al video che compare per primo nel set di file multimediali. I video successivi vengono riprodotti senza didascalie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

Riferimento per set di file multimediali singolo:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample")
```

Set di supporti esplicito:

```
<instance>.setAsset("Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;")
```

Modificatore nitidezza aggiunto a tutte le immagini del set:

```
<instance>.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample?op_sharpen=1")
```

