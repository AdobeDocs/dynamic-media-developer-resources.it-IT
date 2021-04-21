---
description: L'icona di riproduzione viene sovrapposta all'area di visualizzazione principale. Viene visualizzato quando il video viene messo in pausa o quando viene raggiunta la fine del video e dipende anche dal parametro iconeffect .
solution: Experience Manager
title: Icona, effetto
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 1%

---


# Effetto icona{#icon-effect}

L&#39;icona di riproduzione viene sovrapposta all&#39;area di visualizzazione principale. Viene visualizzato quando il video viene messo in pausa o quando viene raggiunta la fine del video e dipende anche dal parametro iconeffect .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspetto dell’icona di riproduzione viene controllato con il seguente selettore di classe CSS:

```
.s7videoviewer . s7videoplayer .s7iconeffect
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
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
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
.s7videoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```

