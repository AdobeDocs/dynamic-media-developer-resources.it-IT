---
description: Il lettore video è l’area rettangolare in cui il contenuto video viene visualizzato nel visualizzatore.
seo-description: Il lettore video è l’area rettangolare in cui il contenuto video viene visualizzato nel visualizzatore.
seo-title: Lettore video
solution: Experience Manager
title: Lettore video
topic: Dynamic media
uuid: d7431a7b-6078-45d6-a364-434b3b44ecf4
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# Lettore video{#video-player}

Il lettore video è l’area rettangolare in cui il contenuto video viene visualizzato nel visualizzatore.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se le dimensioni del video in corso di riproduzione non corrispondono alle dimensioni del lettore video, il contenuto video viene centrato all’interno dell’area di visualizzazione rettangolare del lettore video.

Il seguente selettore di classe CSS controlla l&#39;aspetto del lettore video:

```
.s7mixedmediaviewer .s7videoplayer
```

**Proprietà CSS del lettore video**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del lettore video. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il messaggio di errore visualizzato se il sistema non è in grado di riprodurre il video può essere localizzato. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Esempio: per rendere trasparente il lettore video:

```
.s7mixedmediaviewer .s7videoplayer { 
 background-color: transparent; 
}
```

Le didascalie vengono inserite nel contenitore interno all&#39;interno del lettore video. La posizione di tale contenitore è controllata dagli operatori di posizionamento WebVTT supportati. Il testo della didascalia è all&#39;interno del contenitore; il relativo stile è controllato dal seguente selettore di classe CSS:

```
.s7mixedmediaviewer .s7videoplayer .s7caption
```

**Proprietà CSS delle didascalie**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Sfondo testo didascalia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore del testo della didascalia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p>Spessore font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di font. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare il testo della didascalia su uno sfondo nero semi-trasparente da 14 pixel grigio Arial:

```
.s7mixedmediaviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

L&#39;aspetto dell&#39;animazione del buffering è controllato dal seguente selettore di classe CSS:

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> Margine sinistro dell'icona dell'animazione, in genere meno metà della larghezza dell'icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Margine superiore dell'icona dell'animazione, in genere meno metà dell'altezza dell'icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Manopola la grafica. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un’animazione di buffering su una larghezza di 101 pixel e un’altezza di 29 pixel:

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

