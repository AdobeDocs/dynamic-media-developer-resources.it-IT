---
title: Area visualizzatore principale
description: L’area di visualizzazione principale è occupata dal ritaglio video intelligente. In genere viene impostato per adattarsi allo schermo del dispositivo disponibile quando non è specificata alcuna dimensione.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: c8ea6698-e425-491f-8413-2260ddf40c33
TQID: 'https://experienceleague.adobe.com/m3jZ1-S4Y-1fJJBKvCrrpPi2I9pFEchDMaGhRI-0yBM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 0%

---

# Area visualizzatore principale{#main-viewer-area}

L&#39;area di visualizzazione principale è occupata dal video. In genere viene impostato per adattarsi allo schermo del dispositivo disponibile quando non è specificata alcuna dimensione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Il seguente selettore di classe CSS controlla l&#39;aspetto dell&#39;area di visualizzazione:

```
.s7smartcropvideoviewer 
```

## Proprietà CSS dell&#39;area visualizzatore principale {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo in formato esadecimale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un visualizzatore video con ritaglio avanzato con sfondo bianco (#FFFFFF) e impostarne le dimensioni a 512 x 288 pixel:

```
.s7smartcropvideoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
