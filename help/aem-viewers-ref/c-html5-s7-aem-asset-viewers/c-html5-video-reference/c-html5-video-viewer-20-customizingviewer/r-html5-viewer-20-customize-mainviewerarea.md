---
description: L'area di visualizzazione principale è occupata dal video. In genere viene impostato per adattarsi alla schermata del dispositivo disponibile quando non viene specificata alcuna dimensione.
solution: Experience Manager
title: Area visualizzatore principale
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video
role: Developer,Business Practitioner
exl-id: 7d1379c1-7746-4f61-92df-e8ac4ab7d506
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# Area visualizzatore principale{#main-viewer-area}

L&#39;area di visualizzazione principale è occupata dal video. In genere viene impostato per adattarsi alla schermata del dispositivo disponibile quando non viene specificata alcuna dimensione.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Il seguente selettore di classe CSS controlla l’aspetto dell’area di visualizzazione:

```
.s7videoviewer 
```

## Proprietà CSS dell’area visualizzatore principale {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo in formato esadecimale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un visualizzatore video con sfondo bianco (#FFFFFF) e impostarne le dimensioni di 512 x 288 pixel:

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
