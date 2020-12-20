---
description: L’indicatore di zoom è sovrapposto all’area di visualizzazione principale. Viene visualizzata quando l’immagine è in stato di ripristino e dipende anche dal parametro iconeffect.
seo-description: L’indicatore di zoom è sovrapposto all’area di visualizzazione principale. Viene visualizzata quando l’immagine è in stato di ripristino e dipende anche dal parametro iconeffect.
seo-title: Effetto Icona
solution: Experience Manager
title: Effetto Icona
topic: Dynamic media
uuid: 5daf15ec-fcc5-4e37-924e-9a2cd6c0d167
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 1%

---


# Effetto icona{#icon-effect}

L’indicatore di zoom è sovrapposto all’area di visualizzazione principale. Viene visualizzata quando l’immagine è in stato di ripristino e dipende anche dal parametro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;area di visualizzazione è controllato dal seguente selettore di classe CSS:

```
.s7zoomviewer .s7zoomview .s7iconeffect
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
   <td colname="col2"> <p> Grafica dell’indicatore di zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza indicatore zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza indicatore zoom. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L&#39;effetto Icon supporta il selettore di attributi `media-type`, che può essere utilizzato per applicare effetti di icona diversi su dispositivi diversi. In particolare, `media-type='standard'` corrisponde ai sistemi desktop in cui l&#39;input del mouse viene normalmente utilizzato e `media-type='multitouch'` corrisponde ai dispositivi con ingresso touch.

Esempio: per impostare un indicatore di zoom da 100 x 100 pixel con grafica diversa per i sistemi desktop e i dispositivi touch.

```
.s7zoomviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7zoomviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7zoomviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```

