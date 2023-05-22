---
title: Barra di controllo
description: La barra di controllo è l'area rettangolare che contiene e si trova dietro tutti i controlli dell'interfaccia utente disponibili per il visualizzatore video, ad esempio il pulsante di riproduzione/pausa e i controlli del volume.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2239307a-4a05-4392-b35c-a64ea6c938ad
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 1%

---

# Barra di controllo{#control-bar}

La barra di controllo è l&#39;area rettangolare che contiene e si trova dietro tutti i controlli dell&#39;interfaccia utente disponibili per il visualizzatore video, ad esempio il pulsante di riproduzione/pausa e i controlli del volume.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barra di controllo accetta sempre l’intera larghezza disponibile del visualizzatore. È possibile modificarne il colore, l’altezza e la posizione verticale in base agli stili CSS, rispetto al contenitore del visualizzatore video.

Il seguente selettore di classe CSS controlla l&#39;aspetto della barra di controllo:

```
.s7videoviewer .s7controlbar
```

## Proprietà CSS della barra di controllo {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo inferiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della barra di controllo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un visualizzatore video con una barra di controllo grigia alta 30 pixel e posizionata nella parte superiore del relativo contenitore.

```
.s7videoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
