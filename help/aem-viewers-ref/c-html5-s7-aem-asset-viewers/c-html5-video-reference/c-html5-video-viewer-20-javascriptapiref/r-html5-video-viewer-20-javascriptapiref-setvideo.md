---
title: setVideo
description: Riferimento API di JavaScript per il visualizzatore video
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c89099f6-09f7-4d81-939e-90ffa2764c8c
TQID: 'https://experienceleague.adobe.com/WORlnQXgJ5mDij0ZpNKfpETqHcbKkgLI0N4bJN-T4cw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# setVideo{#setvideo}

Riferimento API di JavaScript per il visualizzatore video

`setVideo(videoUrl[, data])`

Imposta il nuovo video esterno e dati video aggiuntivi facoltativi. Può essere chiamato in qualsiasi momento, sia prima che dopo `init()`. Se chiamato dopo `init()`, il visualizzatore scambia il video in fase di esecuzione.

Vedi anche [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

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

```javascript {.line-numbers}
<instance>.setVideo("https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html")
```
-->
