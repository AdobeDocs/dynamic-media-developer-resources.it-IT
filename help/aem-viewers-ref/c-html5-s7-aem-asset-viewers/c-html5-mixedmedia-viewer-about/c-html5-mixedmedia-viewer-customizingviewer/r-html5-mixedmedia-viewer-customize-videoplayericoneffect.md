---
description: L’icona di riproduzione è sovrapposta all’area di visualizzazione del video. Viene visualizzato quando il video viene messo in pausa o quando viene raggiunta la fine del video, e dipende anche dal parametro iconeffect.
seo-description: L’icona di riproduzione è sovrapposta all’area di visualizzazione del video. Viene visualizzato quando il video viene messo in pausa o quando viene raggiunta la fine del video, e dipende anche dal parametro iconeffect.
seo-title: Effetto icona lettore video
solution: Experience Manager
title: Effetto icona lettore video
topic: Dynamic media
uuid: 5d59c4b2-a7a1-49e1-84c7-0e127a571c4f
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Effetto icona lettore video{#video-player-icon-effect}

L’icona di riproduzione è sovrapposta all’area di visualizzazione del video. Viene visualizzato quando il video viene messo in pausa o quando viene raggiunta la fine del video, e dipende anche dal parametro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L&#39;aspetto dell&#39;icona di riproduzione è controllato dal seguente selettore di classe CSS:

```
.s7mixedmediaviewer . s7videoplayer .s7iconeffect
```

**Proprietà CSS dell&#39;icona di riproduzione**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per l'icona di riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza dell’icona di riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell’icona di riproduzione. </p> </td> 
  </tr> 
 </tbody> 
</table>

L&#39;effetto Icon supporta il selettore di attributi `state`. `state="play"` viene utilizzato quando il video viene messo in pausa al centro della riproduzione e  `state="replay"` viene utilizzato quando la testina di riproduzione si trova alla fine del flusso.

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Impostate un’icona di riproduzione di 100 x 100 pixel.

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

