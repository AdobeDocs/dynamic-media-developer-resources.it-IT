---
title: Lettore video
description: Il lettore video con ritaglio avanzato è l’area rettangolare in cui il contenuto video viene visualizzato nel visualizzatore.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Lettore video{#video-player}

Il lettore video con ritaglio avanzato è l’area rettangolare in cui il contenuto video viene visualizzato nel visualizzatore.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se le dimensioni del video in fase di riproduzione non corrispondono a quelle del lettore video con ritaglio avanzato, il contenuto video viene centrato all’interno dell’area di visualizzazione del rettangolo del lettore video con ritaglio avanzato.

Il seguente selettore di classe CSS controlla l’aspetto del lettore video con ritaglio avanzato:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

**Proprietà CSS del lettore video con ritaglio avanzato**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della visualizzazione principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il messaggio di errore visualizzato se il sistema non è in grado di riprodurre il video può essere localizzato. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

Esempio: per impostare un visualizzatore video con ritaglio avanzato con le dimensioni del lettore video con ritaglio avanzato impostate su 512 x 288 pixel.

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

I sottotitoli codificati vengono inseriti in un contenitore interno all’interno del lettore video con ritaglio avanzato. La posizione del contenitore è controllata da operatori di posizionamento WebVTT supportati. Il testo della didascalia si trova all’interno del contenitore e il suo stile è controllato dal seguente selettore di classe CSS:

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

**Proprietà CSS dei sottotitoli**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Sfondo del testo della didascalia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
   <td colname="col2"> <p>Colore testo sottotitoli. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p> Spessore font sottotitoli codificati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> Dimensione font sottotitoli. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p>Font per sottotitoli. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare il testo dei sottotitoli codificati su 14 pixel, grigio chiaro, Arial®, su uno sfondo nero semitrasparente:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

L’aspetto dell’animazione di buffering è controllato dal seguente selettore di classe CSS:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon
```

**Proprietà CSS dell&#39;icona Attendi**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p> Larghezza icona animazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p> Altezza icona animazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine sinistro </span> </p> </td> 
   <td colname="col2"> <p> Margine sinistro dell'icona di animazione, in genere meno la metà della larghezza dell'icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine superiore </span> </p> </td> 
   <td colname="col2"> <p> Margine superiore dell'icona di animazione, in genere meno la metà dell'altezza dell'icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Grafica a manopola. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un’animazione di buffering su una larghezza di 101 pixel e un’altezza di 29 pixel:

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
