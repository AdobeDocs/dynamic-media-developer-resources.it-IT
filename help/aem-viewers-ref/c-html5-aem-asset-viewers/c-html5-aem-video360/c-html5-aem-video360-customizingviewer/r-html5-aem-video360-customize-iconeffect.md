---
title: Effetto icona
description: L'icona di riproduzione è sovrapposta all'area di visualizzazione principale. Viene visualizzato quando il video viene messo in pausa o quando viene raggiunta la fine del video, e dipende anche dal parametro iconeffect.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e25a3b9d-88ef-4214-9b6b-2527ebf0f145
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 1%

---

# Effetto icona{#icon-effect}

L&#39;icona di riproduzione è sovrapposta all&#39;area di visualizzazione principale. Viene visualizzato quando il video viene messo in pausa o quando viene raggiunta la fine del video, e dipende anche dal parametro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

L’aspetto dell’icona di riproduzione è controllato dal seguente selettore di classe CSS:

```
.s7video360viewer . s7video360player .s7iconeffect
```

**Proprietà CSS dell’icona Riproduci**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per l'icona di riproduzione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Consulta <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
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

L&#39;effetto Icona supporta `state` selettore di attributi. Selettore di attributi `state="play"` viene utilizzato quando il video viene messo in pausa nel mezzo della riproduzione e `state="replay"` viene utilizzato quando la testina di riproduzione si trova alla fine del flusso.

**Esempio** : imposta un&#39;icona di riproduzione di 100 x 100 pixel.

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
