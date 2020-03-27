---
description: L'area di visualizzazione principale è occupata dal video. In genere viene impostato per adattarsi allo schermo del dispositivo disponibile quando non vengono specificate dimensioni.
seo-description: L'area di visualizzazione principale è occupata dal video. In genere viene impostato per adattarsi allo schermo del dispositivo disponibile quando non vengono specificate dimensioni.
seo-title: Area visualizzatore principale
solution: Experience Manager
title: Area visualizzatore principale
topic: Dynamic media
uuid: f395b22d-55b8-4422-9aa4-9dd4b7a24063
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Area visualizzatore principale{#main-viewer-area}

L&#39;area di visualizzazione principale è occupata dal video. In genere viene impostato per adattarsi allo schermo del dispositivo disponibile quando non vengono specificate dimensioni.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Il seguente selettore di classe CSS controlla l&#39;aspetto dell&#39;area di visualizzazione:

```
.s7videoviewer 
```

## Proprietà CSS dell&#39;area visualizzatore principale {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo in formato esadecimale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un visualizzatore video con uno sfondo bianco (#FFFFFF) e impostarne le dimensioni di 512 x 288 pixel:

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

