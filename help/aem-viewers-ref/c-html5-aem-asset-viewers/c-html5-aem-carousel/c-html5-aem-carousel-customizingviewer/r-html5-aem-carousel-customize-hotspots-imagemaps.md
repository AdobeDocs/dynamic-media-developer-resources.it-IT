---
description: Il visualizzatore visualizza le icone dei punti attivi sopra la vista principale, nei punti in cui i punti attivi erano originariamente creati in Dynamic Media di  AEM Assets - su richiesta.
seo-description: Il visualizzatore visualizza le icone dei punti attivi sopra la vista principale, nei punti in cui i punti attivi erano originariamente creati in Dynamic Media di  AEM Assets - su richiesta.
seo-title: Punti attivi e mappe immagine
solution: Experience Manager
title: Punti attivi e mappe immagine
topic: Dynamic media
uuid: de7f4dc7-1a55-49d5-a712-7f178cc49068
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---


# Punti attivi e mappe immagine{#hotspots-and-image-maps}

Il visualizzatore visualizza le icone dei punti attivi sopra la vista principale, nei punti in cui i punti attivi erano originariamente creati in Dynamic Media di  AEM Assets - su richiesta.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;icona del punto di attivazione è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Grafica dell'icona del punto di attivazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>Posizionarsi all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Vedere <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza icona punto di attivazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza icona punto di attivazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: impostate un’icona di un punto attivo da 56x56 pixel che mostra un’immagine diversa per ciascuno dei due stati di icona:

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

**Proprietà CSS dell&#39;area della mappa immagine**

L&#39;aspetto dell&#39;area della mappa immagine è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p>Colore di riempimento area mappa immagine </p> <p>Specificate questo colore nei formati <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> o <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Colore di riempimento area mappa immagine </p> <p>Specificate questo colore nei formati <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) </span> o <span class="codeph"> RGBA(R,G,B,A) </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Stile del bordo della mappa immagine. Deve essere specificato come " <span class="codeph"> larghezza </span> <span class="codeph"> colore in tinta unita </span>", dove <span class="codeph"> larghezza </span> è espressa in pixel, e <span class="codeph"> colore </span> è impostato come <span class="codeph"> #RRGGBB </span>, <span class="codeph"> RGB(R,G,B) &lt;a1/&gt; oppure <span class="codeph"> RGBA(R,G,B,A) </span>.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: imposta un&#39;area di mappa immagine trasparente con un bordo nero di un pixel:

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

