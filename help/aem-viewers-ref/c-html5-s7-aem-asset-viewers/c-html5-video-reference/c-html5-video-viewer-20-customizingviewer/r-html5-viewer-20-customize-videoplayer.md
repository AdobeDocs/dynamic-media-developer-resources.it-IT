---
title: Lettore video
description: Il lettore video è l’area rettangolare in cui il contenuto video viene visualizzato all’interno del visualizzatore.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2741821f-78fe-44d4-8604-fee10086e0a0
TQID: 'https://experienceleague.adobe.com/mVDQWuBQZT9--O4V3XCrPRasFvG8x7fIsxqQLFsMpNU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 310
ht-degree: 0%

---

# Lettore video{#video-player}

Il lettore video è l’area rettangolare in cui il contenuto video viene visualizzato all’interno del visualizzatore.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se le dimensioni del video che viene riprodotto non corrispondono a quelle del lettore video, il contenuto video è centrato all’interno dell’area di visualizzazione del rettangolo del lettore video.

Il seguente selettore di classe CSS controlla l’aspetto del lettore video:

```
.s7videoviewer .s7videoplayer
```

**Proprietà CSS del lettore video**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della visualizzazione principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il messaggio di errore visualizzato se il sistema non è in grado di riprodurre il video può essere localizzato. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

Esempio: per impostare un visualizzatore video con le dimensioni del lettore video impostate su 512 x 288 pixel.

```
.s7videoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

I sottotitoli codificati vengono inseriti in un contenitore interno del lettore video. La posizione del contenitore è controllata da operatori di posizionamento WebVTT supportati. Il testo della didascalia si trova all’interno del contenitore e il suo stile è controllato dal seguente selettore di classe CSS:

`. s7videoviewer .s7 videoplayer .s7caption`

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
.s7videoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

L’aspetto dell’animazione di buffering è controllato dal seguente selettore di classe CSS:

```
.s7videoviewer .s7videoplayer .s7waiticon
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
.s7videoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
