---
description: La barra di controllo è l’area rettangolare che contiene e si trova dietro tutti i controlli dell’interfaccia utente disponibili per il visualizzatore video, ad esempio il pulsante di riproduzione/pausa, i controlli del volume e così via.
solution: Experience Manager
title: Barra di controllo
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: f0de655c-36f0-4ed4-806c-d486eed2201b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---

# Barra di controllo{#control-bar}

La barra di controllo è l’area rettangolare che contiene e si trova dietro tutti i controlli dell’interfaccia utente disponibili per il visualizzatore video, ad esempio il pulsante di riproduzione/pausa, i controlli del volume e così via.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barra di controllo occupa sempre l’intera larghezza del visualizzatore disponibile. È possibile modificarne il colore, l’altezza e la posizione verticale per CSS, rispetto al contenitore del visualizzatore video.

Il seguente selettore di classe CSS controlla l’aspetto della barra di controllo:

```
.s7mixedmediaviewer .s7controlbar
```

## Proprietà CSS della barra di controllo {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della barra di controllo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un visualizzatore per file multimediali diversi con una barra di controllo grigia alta 30 pixel.

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
