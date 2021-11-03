---
title: Scorrimento video
description: Lo scorrimento video è il dispositivo di scorrimento orizzontale che consente all'utente di cercare in modo dinamico qualsiasi posizione temporale all'interno del video attualmente in riproduzione.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 404e39d4-565e-4dde-b2bd-fa83a895d001
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---

# Scorrimento video{#video-scrubber}

Lo scorrimento video è il dispositivo di scorrimento orizzontale che consente all&#39;utente di cercare in modo dinamico qualsiasi posizione temporale all&#39;interno del video attualmente in riproduzione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La manopola di scorrimento si sposta anche durante la riproduzione del video per indicare la posizione temporale corrente del video durante la riproduzione. Lo scorrimento video occupa sempre l&#39;intera larghezza della barra di controllo. È possibile eseguire lo scorrimento del video, modificarne l&#39;altezza e la posizione verticale tramite CSS.

L’aspetto generale dello scorrimento video è controllato con il seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7videoscrubber 
.s7smartcropvideoviewer .s7videoscrubber .s7videotime 
.s7smartcropvideoviewer .s7videoscrubber .s7knob
```

**Proprietà CSS dello scorrimento video**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo inferiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dello scorrimento video. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore dello scorrimento video. </p> </td> 
  </tr> 
 </tbody> 
</table>

I seguenti selettori di classe CSS tengono traccia degli indicatori di sfondo, riproduzione e caricamento:

```
.s7smartcropvideoviewer .s7videoscrubber .s7track 
.s7smartcropvideoviewer .s7videoscrubber .s7trackloaded 
.s7smartcropvideoviewer .s7videoscrubber .s7trackplayed
```

**Proprietà CSS del brano**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza del brano corrispondente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore del brano corrispondente. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il seguente selettore di classe CSS controlla la manopola:

```
.s7smartcropvideoviewer .s7videoscrubber .s7knob
```

**Proprietà CSS della manopola**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Offset a manopola verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della manopola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza della manopola. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Lavori d'arte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il seguente selettore di classe CSS controlla la bolla temporale riprodotta:

```
.s7smartcropvideoviewer .s7videoscrubber .s7videotime
```

**Proprietà CSS della bolla temporale riprodotta**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> Famiglia di font da utilizzare per il testo di visualizzazione dell'ora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> Dimensione del font da utilizzare per il testo visualizzato in base all'ora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Il colore del font da utilizzare per il testo visualizzato in base all'ora. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza area bolla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell'area della bolla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura dell'area della bolla. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Illustrazione a bolle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Allineamento del testo con l'area della bolla. </p> </td> 
  </tr> 
 </tbody> 
</table>

È possibile localizzare la descrizione comandi per lo scorrimento video. Vedi [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) per ulteriori informazioni.

**Esempio** - Per impostare un visualizzatore video con uno scorrimento video con colori di traccia personalizzati alti dieci pixel. Infine, posizionarlo a 10 pixel e 35 pixel dai bordi superiore e sinistro della barra di controllo.

```
.s7smartcropvideoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```
