---
description: L'indicatore di rotazione viene sovrapposto all'area di visualizzazione di rotazione. Viene visualizzato quando l’immagine è in uno stato di reset e dipende anche dal parametro iconeffect .
solution: Experience Manager
title: Effetto icona a forma di ruota
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,User
exl-id: 1c5c73f9-c32a-4bca-93f0-c5a95756355b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%

---

# Effetto icona a forma di ruota{#spin-view-icon-effect}

L&#39;indicatore di rotazione viene sovrapposto all&#39;area di visualizzazione di rotazione. Viene visualizzato quando l’immagine è in uno stato di reset e dipende anche dal parametro iconeffect .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato con il seguente selettore di classe CSS:

```
.s7mixedmediaviewer .s7spinview .s7iconeffect
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
   <td colname="col2"> <p> Grafico indicatore a 360 gradi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza indicatore a 360 gradi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza indicatore a 360 gradi. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’indicatore a 360 gradi supporta il selettore di attributi `state` impostato su `spin_1D` in caso di set a 360 gradi monodimensionali e su `spin_2D` in caso di set a 360 gradi multidimensionali.

Esempio: per impostare un indicatore di zoom di 100 x 100 pixel.

```
.s7mixedmediaviewer .s7spinview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7spinview .s7iconeffect[state="spin_1D"] { 
background-image: url(images/spinIcon_1D.png); 
} 
.s7mixedmediaviewer .s7spinview .s7iconeffect[state="spin_2D"] { 
background-image: url(images/spinIcon_2D.png); 
}
```
