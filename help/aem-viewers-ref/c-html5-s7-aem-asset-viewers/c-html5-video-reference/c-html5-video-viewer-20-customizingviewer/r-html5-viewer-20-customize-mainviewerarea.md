---
description: L'area di visualizzazione principale è occupata dal video. In genere viene impostato per adattarsi alla schermata del dispositivo disponibile quando non viene specificata alcuna dimensione.
solution: Experience Manager
title: Area visualizzatore principale
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '111'
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

