---
title: Icona, effetto
description: L'icona di riproduzione viene sovrapposta all'area di visualizzazione principale. Viene visualizzato quando il video viene messo in pausa o quando viene raggiunta la fine del video e dipende anche dal parametro iconeffect .
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 1%

---

# Icona, effetto{#icon-effect}

L&#39;icona di riproduzione viene sovrapposta all&#39;area di visualizzazione principale. Viene visualizzato quando il video viene messo in pausa o quando viene raggiunta la fine del video e dipende anche dal parametro iconeffect .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspetto dell’icona di riproduzione viene controllato con il seguente selettore di classe CSS:

```
.s7smartcropvideoviewer . s7smartcropvideoplayer .s7iconeffect
```

**Proprietà CSS dell’icona di riproduzione**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per l’icona di riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
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

L&#39;effetto icona supporta `state` selettore di attributi. `state="play"` viene utilizzato quando il video viene messo in pausa al centro della riproduzione, e `state="replay"` viene utilizzato quando la testina di riproduzione si trova alla fine del flusso.

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Imposta un&#39;icona di riproduzione di 100 x 100 pixel.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
