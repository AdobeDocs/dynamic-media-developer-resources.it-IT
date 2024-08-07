---
title: Barra di controllo
description: La barra di controllo è l'area rettangolare che contiene e si trova dietro tutti i controlli dell'interfaccia utente disponibili per il visualizzatore video, ad esempio il pulsante di riproduzione/pausa e i controlli del volume.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 06078310-8aeb-449f-919a-ce88ddc8c4b3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# Barra di controllo{#control-bar}

La barra di controllo è l&#39;area rettangolare che contiene e si trova dietro tutti i controlli dell&#39;interfaccia utente disponibili per il visualizzatore video, ad esempio il pulsante di riproduzione/pausa e i controlli del volume.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La barra di controllo accetta sempre l’intera larghezza disponibile del visualizzatore. È possibile modificarne il colore, l’altezza e la posizione verticale in base agli stili CSS, rispetto al contenitore del visualizzatore video.

Il seguente selettore di classe CSS controlla l&#39;aspetto della barra di controllo:

```
.s7video360viewer .s7controlbar
```

## Proprietà CSS della barra di controllo {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primi </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> in basso </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo inferiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza della barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della barra di controllo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** - Per impostare un visualizzatore video con una barra di controllo grigia alta 30 pixel e posizionata nella parte superiore del contenitore del visualizzatore video.

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
