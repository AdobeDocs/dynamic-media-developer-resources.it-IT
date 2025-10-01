---
title: setVideo
description: Riferimento API di JavaScript per il visualizzatore video Ritaglio avanzato
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 5e735e11-e359-4b98-b4a9-2c69a8eb424a
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---

# setVideo{#setvideo}

Riferimento API di JavaScript per il visualizzatore video Ritaglio avanzato

`setVideo(videoUrl[, data])`

Imposta il nuovo video esterno e dati video aggiuntivi facoltativi. Può essere chiamato in qualsiasi momento, sia prima che dopo `init()`. Se chiamato dopo `init()`, il visualizzatore scambia il video in fase di esecuzione.

Vedi anche [init]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## Parametri {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> Stringa </span>} URL assoluto del nuovo video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dati </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} oggetto JSON con i seguenti campi facoltativi (distinzione maiuscole/minuscole): </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> immagine posteriore </span> - Immagine da visualizzare sul primo fotogramma prima che inizi la riproduzione del video. Vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> didascalia </span> - Posizione del nuovo file di didascalia. Se non viene specificato alcun file di didascalia, il pulsante della didascalia non viene visualizzato nell'interfaccia utente. </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> Navigazione <span class="codeph"> </span> - URL o percorso del contenuto di navigazione WebVTT. Il file WebVTT deve essere gestito da Image Server. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

<!--
## Example {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```
-->
