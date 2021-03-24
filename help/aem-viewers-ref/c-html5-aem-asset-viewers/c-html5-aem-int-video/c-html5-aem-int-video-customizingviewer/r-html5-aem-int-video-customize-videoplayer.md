---
description: Il lettore video è l’area rettangolare in cui il contenuto video viene visualizzato all’interno del visualizzatore.
solution: Experience Manager
title: Lettore video
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 1%

---


# Lettore video{#video-player}

Il lettore video è l’area rettangolare in cui il contenuto video viene visualizzato all’interno del visualizzatore.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se le dimensioni del video in corso di riproduzione non corrispondono alle dimensioni del lettore video, il contenuto video viene centrato all’interno dell’area di visualizzazione rettangolare del lettore video.

Il seguente selettore di classe CSS controlla l’aspetto del lettore video:

```
.s7interactivevideoviewer .s7videoplayer
```

**Proprietà CSS del lettore video**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

È possibile localizzare il messaggio di errore visualizzato nei casi in cui il sistema non è in grado di riprodurre il video.

Consulta [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Esempio: per impostare un visualizzatore video con le dimensioni del lettore video impostate su 512 x 288 pixel.

```
.s7interactivevideoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

I sottotitoli codificati vengono inseriti in un contenitore interno all’interno del lettore video. La posizione del contenitore è controllata dagli operatori di posizionamento WebVTT supportati. Il testo della didascalia si trova all’interno del contenitore e il relativo stile è controllato con il seguente selettore di classe CSS:

`.s7interactivevideoviewer .s7videoplayer .s7caption`

**Proprietà CSS dei sottotitoli**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Sfondo testo sottotitoli. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Chiudi il colore del testo della didascalia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight  </span> </p> </td> 
   <td colname="col2"> <p> Spessore font didascalia chiusa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p> Dimensione del font della didascalia chiusa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Font per sottotitoli codificati. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-5b82913ff3c44b7b8187969cb15e9560}

Per impostare un testo dei sottotitoli codificati a 14 pixel, grigio chiaro, Arial, su uno sfondo nero semitrasparente:

```
.s7interactivevideoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

L’aspetto dell’animazione di buffering è controllato con il seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon
```

**Proprietà CSS dell’icona di attesa**

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
   <td colname="col1"> <p> <span class="codeph"> margine sinistro  </span> </p> </td> 
   <td colname="col2"> <p> Icona di animazione a sinistra del margine, normalmente meno metà della larghezza dell'icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine superiore  </span> </p> </td> 
   <td colname="col2"> <p> Margine superiore dell'icona di animazione, normalmente meno metà dell'altezza dell'icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Lavori d'arte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un’animazione buffering su una larghezza di 101 pixel e un’altezza di 29 pixel:

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

