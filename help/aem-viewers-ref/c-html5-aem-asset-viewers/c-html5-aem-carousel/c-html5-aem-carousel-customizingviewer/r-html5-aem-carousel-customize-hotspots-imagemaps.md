---
description: Il visualizzatore visualizza le icone dei punti attivi sopra la visualizzazione principale nei luoghi in cui i punti attivi sono stati originariamente creati in Dynamic Media di AEM Assets - on-demand.
seo-description: Il visualizzatore visualizza le icone dei punti attivi sopra la visualizzazione principale nei luoghi in cui i punti attivi sono stati originariamente creati in Dynamic Media di AEM Assets - on-demand.
seo-title: Hotspot e mappe immagine
solution: Experience Manager
title: Hotspot e mappe immagine
uuid: de7f4dc7-1a55-49d5-a712-7f178cc49068
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 1%

---


# Punti attivi e mappe immagine{#hotspots-and-image-maps}

Il visualizzatore visualizza le icone dei punti attivi sopra la visualizzazione principale nei luoghi in cui i punti attivi sono stati originariamente creati in Dynamic Media di AEM Assets - on-demand.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’icona del punto attivo è controllato con il seguente selettore di classe CSS:

```
.s7carouselviewer .s7imagemapeffect .s7icon
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Immagine icona punto attivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Posizionare all’interno dello sprite dell’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza icona punto attivo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza icona punto attivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio : imposta un’icona punto attivo da 56 x 56 pixel che mostra un’immagine diversa per ciascuno dei due stati dell’icona:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

**Proprietà CSS dell’area mappa immagine**

L’aspetto dell’area della mappa immagine è controllato con il seguente selettore di classe CSS:

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore di riempimento area mappa immagine. </p> <p>Specificare questo colore nei formati <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> o <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore di riempimento area mappa immagine. </p> <p>Specificare questo colore nei formati <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> o <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Stile del bordo della regione mappa immagine. Deve essere specificato come " <span class="codeph"> larghezza </span> <span class="codeph"> colore solido </span>", dove <span class="codeph"> larghezza </span> è espressa in pixel, e <span class="codeph"> colore </span> è impostato come <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> o <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: imposta un&#39;area mappa immagine trasparente con un bordo nero da un pixel:

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

