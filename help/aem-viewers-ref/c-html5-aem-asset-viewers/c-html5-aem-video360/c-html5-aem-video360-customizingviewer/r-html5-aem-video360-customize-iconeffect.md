---
title: Icon effect
description: L'icona di riproduzione viene sovrapposta all'area di visualizzazione principale. It displays when the video is paused, or when the end of the video is reached, and it also depends on the iconeffect parameter.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e25a3b9d-88ef-4214-9b6b-2527ebf0f145
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 1%

---

# Icon effect{#icon-effect}

The play icon is overlaid on the main view area. Viene visualizzato quando il video viene messo in pausa o quando viene raggiunta la fine del video e dipende anche dal parametro iconeffect .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

The appearance of the play icon is controlled with the following CSS class selector:

```
.s7video360viewer . s7video360player .s7iconeffect
```

**Proprietà CSS dell’icona di riproduzione**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> The displayed image for the play icon. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza dell'icona di riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>The height of the play icon. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’effetto icona supporta il selettore di attributi `state`. Il selettore di attributi `state="play"` viene utilizzato quando il video viene messo in pausa al centro della riproduzione e `state="replay"` viene utilizzato quando la testina di riproduzione si trova alla fine del flusso.

**Example** - Setup a 100 x 100 pixel play icon.

```
.s7video360viewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
