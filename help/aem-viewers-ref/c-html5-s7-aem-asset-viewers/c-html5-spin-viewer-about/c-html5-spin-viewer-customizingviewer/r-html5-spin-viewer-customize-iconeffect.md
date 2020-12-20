---
description: L’indicatore 360 gradi viene sovrapposto all’area di visualizzazione principale. Viene visualizzata quando l’immagine è in stato di reimpostazione e dipende anche dal parametro dell’effetto icona.
seo-description: L’indicatore 360 gradi viene sovrapposto all’area di visualizzazione principale. Viene visualizzata quando l’immagine è in stato di reimpostazione e dipende anche dal parametro dell’effetto icona.
seo-title: Effetto Icona
solution: Experience Manager
title: Effetto Icona
topic: Dynamic media
uuid: ce0524e4-fff4-45b0-8069-d5876802d66f
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 1%

---


# Effetto icona{#icon-effect}

L’indicatore 360 gradi viene sovrapposto all’area di visualizzazione principale. Viene visualizzata quando l’immagine è in stato di reimpostazione e dipende anche dal parametro dell’effetto icona.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto dell&#39;area di visualizzazione è controllato dal seguente selettore di classe CSS:

```
.s7spinviewer .s7spinview .s7iconeffect
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
   <td colname="col2"> <p> Grafica indicatore 360 gradi </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza indicatore 360 gradi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza indicatore 360 gradi. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’indicatore 360 gradi supporta il selettore di attributi `state` impostato su `spin_1D` nel caso di set 360 gradi monodimensionali e su `spin_2D` nel caso di set 360 gradi multidimensionali.

Esempio: per impostare un indicatore di zoom di 100 x 100 pixel.

```
.s7spinviewer .s7spinview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7spinviewer .s7spinview .s7iconeffect[state="spin_1D"] { 
background-image: url(images/spinIcon_1D.png); 
} 
.s7spinviewer .s7spinview .s7iconeffect[state="spin_2D"] { 
background-image: url(images/spinIcon_2D.png); 
}
```

