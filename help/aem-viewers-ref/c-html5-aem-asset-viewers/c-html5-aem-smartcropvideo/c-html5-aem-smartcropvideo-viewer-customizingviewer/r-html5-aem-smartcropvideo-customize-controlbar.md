---
description: La barra di controllo è l’area rettangolare che contiene e si trova dietro tutti i controlli dell’interfaccia utente disponibili per il visualizzatore Smart Crop Video, ad esempio il pulsante di riproduzione/pausa, i controlli del volume e così via.
solution: Experience Manager
title: Barra di controllo
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2239307a-4a05-4392-b35c-a64ea6c938ad
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---

# Barra di controllo{#control-bar}

La barra di controllo è l’area rettangolare che contiene e si trova dietro tutti i controlli dell’interfaccia utente disponibili per il visualizzatore Smart Crop Video, ad esempio il pulsante di riproduzione/pausa, i controlli del volume e così via.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barra di controllo occupa sempre l’intera larghezza del visualizzatore disponibile. È possibile modificarne il colore, l’altezza e la posizione verticale tramite CSS, rispetto al contenitore del visualizzatore video di ritaglio avanzato.

Il seguente selettore di classe CSS controlla l’aspetto della barra di controllo:

```
.s7smartcropvideoviewer .s7controlbar
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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della barra di controllo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un visualizzatore video Ritaglio avanzato con una barra di controllo grigia alta 30 pixel e posizionato nella parte superiore del contenitore del visualizzatore video Ritaglio avanzato.

```
.s7smartcropvideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
