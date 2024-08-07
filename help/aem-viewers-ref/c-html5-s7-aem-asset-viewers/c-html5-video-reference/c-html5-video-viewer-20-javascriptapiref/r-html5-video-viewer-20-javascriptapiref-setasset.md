---
title: setAsset
description: Guida di riferimento dell’API JavaScript per il visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e5d71393-fcae-4bd4-8e78-a451b2f05ffc
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# setAsset{#setasset}

Guida di riferimento dell’API JavaScript per il visualizzatore video.

`setAsset(asset[, data])`

Imposta la nuova risorsa e dati facoltativi aggiuntivi sulla risorsa. È possibile chiamare questo parametro in qualsiasi momento, prima o dopo `init()`. Se viene chiamato dopo `init()`, il visualizzatore scambia la risorsa in fase di runtime.

Vedi anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parametri {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> risorsa </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Stringa </span>} ID nuova risorsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dati </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} oggetto JSON con i seguenti campi facoltativi (distinzione maiuscole/minuscole): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> immagine posteriore </span> - Immagine da visualizzare sul primo fotogramma prima che inizi la riproduzione del video. Vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> didascalia </span> - percorso del nuovo file di sottotitoli codificati. Se il file non è specificato, il pulsante dei sottotitoli non è visibile nell'interfaccia utente. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> Navigazione <span class="codeph"> </span> - URL o percorso del contenuto di navigazione WebVTT. Il file WebVTT deve essere gestito da Image Server </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```
