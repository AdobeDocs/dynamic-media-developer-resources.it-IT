---
description: L’icona di riproduzione viene sovrapposta all’area di visualizzazione video. Viene visualizzato quando il video viene messo in pausa o quando viene raggiunta la fine del video e dipende anche dal parametro iconeffect .
solution: Experience Manager
title: Effetto icona lettore video
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: 1e0bd97f-20e9-41e6-95fc-d693644152da
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 1%

---

# Effetto icona lettore video{#video-player-icon-effect}

L’icona di riproduzione viene sovrapposta all’area di visualizzazione video. Viene visualizzato quando il video viene messo in pausa o quando viene raggiunta la fine del video e dipende anche dal parametro iconeffect .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspetto dell’icona di riproduzione viene controllato con il seguente selettore di classe CSS:

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**Proprietà CSS dell’icona di riproduzione**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per l’icona di riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza dell'icona di riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell'icona di riproduzione. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’effetto icona supporta il selettore di attributi `state`. `state="play"` viene utilizzato quando il video viene messo in pausa al centro della riproduzione e  `state="replay"` viene utilizzato quando la testina di riproduzione si trova alla fine del flusso.

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Imposta un&#39;icona di riproduzione di 100 x 100 pixel.

```
.s7mixedmediaviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7mixedmediaviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
