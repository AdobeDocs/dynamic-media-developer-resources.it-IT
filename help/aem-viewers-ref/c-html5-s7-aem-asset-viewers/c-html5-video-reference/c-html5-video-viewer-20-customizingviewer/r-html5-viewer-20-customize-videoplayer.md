---
description: Il lettore video è l’area rettangolare in cui il contenuto video viene visualizzato nel visualizzatore.
seo-description: Il lettore video è l’area rettangolare in cui il contenuto video viene visualizzato nel visualizzatore.
seo-title: Lettore video
solution: Experience Manager
title: Lettore video
topic: Dynamic media
uuid: 2748c3d3-b974-4e54-8218-a2ec9e31a668
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video player{#video-player}

Il lettore video è l’area rettangolare in cui il contenuto video viene visualizzato nel visualizzatore.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se le dimensioni del video in corso di riproduzione non corrispondono alle dimensioni del lettore video, il contenuto video viene centrato all’interno dell’area di visualizzazione rettangolare del lettore video.

Il seguente selettore di classe CSS controlla l&#39;aspetto del lettore video:

```
.s7videoviewer .s7videoplayer
```

**Proprietà CSS del lettore video**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il messaggio di errore visualizzato se il sistema non è in grado di riprodurre il video può essere localizzato. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) dell&#39;interfaccia utente.

Esempio: per impostare un visualizzatore video con le dimensioni del lettore video impostate su 512 x 288 pixel.

```
.s7videoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

I sottotitoli codificati vengono inseriti in un contenitore interno all’interno del lettore video. La posizione di tale contenitore è controllata dagli operatori di posizionamento WebVTT supportati. Il testo della didascalia è all&#39;interno del contenitore e il relativo stile è controllato dal seguente selettore di classe CSS:

`. s7videoviewer .s7 videoplayer .s7caption`

**Proprietà CSS dei sottotitoli codificati**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Sfondo del testo dei sottotitoli codificati. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore del testo della didascalia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p> Spessore font didascalia chiusa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> Dimensione font didascalia chiusa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Font per sottotitoli codificati. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un testo di sottotitoli codificati su 14 pixel, grigio chiaro, Arial, su uno sfondo nero semitrasparente:

```
.s7videoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

L&#39;aspetto dell&#39;animazione del buffering è controllato dal seguente selettore di classe CSS:

```
.s7videoviewer .s7videoplayer .s7waiticon
```

**Proprietà CSS dell&#39;icona di attesa**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza icona animazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Altezza icona animazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> Margine sinistro dell'icona dell'animazione, in genere meno metà della larghezza dell'icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> Margine superiore dell'icona dell'animazione, in genere meno metà dell'altezza dell'icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Manopola la grafica. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un’animazione di buffering su una larghezza di 101 pixel e un’altezza di 29 pixel:

```
.s7videoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

