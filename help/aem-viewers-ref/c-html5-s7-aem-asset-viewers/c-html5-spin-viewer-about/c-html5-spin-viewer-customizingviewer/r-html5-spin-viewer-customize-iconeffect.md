---
title: Icona, effetto
description: L'indicatore di rotazione viene sovrapposto all'area di visualizzazione principale. Viene visualizzato quando l’immagine è in uno stato di reset e dipende anche dal parametro iconeffect .
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 1ded69eb-62cd-49da-ab53-124348359a58
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# Icona, effetto{#icon-effect}

L&#39;indicatore di rotazione viene sovrapposto all&#39;area di visualizzazione principale. Viene visualizzato quando l’immagine è in uno stato di reset e dipende anche dal parametro iconeffect .

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato con il seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Grafico indicatore a 360 gradi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
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

L&#39;indicatore a 360 gradi supporta `state` selettore di attributi impostato su `spin_1D` se è presente un set 360 gradi dimensionale singolo, e `spin_2D` se è presente un set 360 gradi multidimensionale.

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
