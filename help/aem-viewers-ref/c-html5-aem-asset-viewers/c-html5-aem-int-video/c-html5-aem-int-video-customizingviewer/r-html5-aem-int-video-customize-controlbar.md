---
description: La barra di controllo è l’area rettangolare che contiene e si trova dietro tutti i controlli dell’interfaccia utente disponibili per il visualizzatore video, ad esempio il pulsante di riproduzione/pausa, i controlli del volume e così via.
seo-description: La barra di controllo è l’area rettangolare che contiene e si trova dietro tutti i controlli dell’interfaccia utente disponibili per il visualizzatore video, ad esempio il pulsante di riproduzione/pausa, i controlli del volume e così via.
seo-title: Barra di controllo
solution: Experience Manager
title: Barra di controllo
topic: Dynamic media
uuid: 1fa90f7d-6b26-499d-8e6c-1cd80405aec0
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# Barra di controllo{#control-bar}

La barra di controllo è l’area rettangolare che contiene e si trova dietro tutti i controlli dell’interfaccia utente disponibili per il visualizzatore video, ad esempio il pulsante di riproduzione/pausa, i controlli del volume e così via.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barra di controllo occupa sempre l’intera larghezza del visualizzatore disponibile. È possibile modificarne il colore, l’altezza e la posizione verticale in CSS, rispetto al contenitore del visualizzatore video.

Il seguente selettore di classe CSS controlla l&#39;aspetto della barra di controllo:

```
.s7interactivevideoviewer .s7controlbar
```

## Proprietà CSS della barra di controllo {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo inferiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della barra di controllo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un visualizzatore video con una barra di controllo grigia alta 30 pixel e nella parte superiore del contenitore del visualizzatore video.

```
.s7interactivevideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

