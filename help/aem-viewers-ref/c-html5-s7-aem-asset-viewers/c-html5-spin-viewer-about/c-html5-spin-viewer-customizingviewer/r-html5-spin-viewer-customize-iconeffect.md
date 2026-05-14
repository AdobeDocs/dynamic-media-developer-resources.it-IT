---
title: Effetto icona
description: L'indicatore di rotazione è sovrapposto all'area di visualizzazione principale. Viene visualizzata quando l'immagine è in stato di ripristino e dipende anche dal parametro iconeffect.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 1ded69eb-62cd-49da-ab53-124348359a58
TQID: 'https://experienceleague.adobe.com/HQJrSNPeLhHNmsRlxsw785h-It00j2zmzSkbtj6lvHQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 152
ht-degree: 0%

---

# Effetto icona{#icon-effect}

L&#39;indicatore di rotazione è sovrapposto all&#39;area di visualizzazione principale. Viene visualizzata quando l&#39;immagine è in stato di ripristino e dipende anche dal parametro iconeffect.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto dell’area di visualizzazione è controllato dal seguente selettore di classi CSS:

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
   <td colname="col2"> <p> Illustrazione dell'indicatore di rotazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza indicatore di rotazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza indicatore di rotazione. </p> </td> 
  </tr> 
 </tbody> 
</table>

L&#39;indicatore di rotazione supporta il selettore di attributi `state` impostato su `spin_1D` se è presente un set 360 gradi monodimensionale e su `spin_2D` se è presente un set 360 gradi multidimensionale.

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
