---
title: Visualizzazione zoom a comparsa
description: La visualizzazione principale consiste nell’immagine statica e nell’immagine ingrandita mostrata nella visualizzazione a comparsa sopra l’immagine statica. È inoltre costituito dal messaggio di suggerimento visualizzato sopra l’immagine statica.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 1%

---

# Visualizzazione zoom a comparsa{#flyout-zoom-view}

La visualizzazione principale consiste nell’immagine statica e nell’immagine ingrandita mostrata nella visualizzazione a comparsa sopra l’immagine statica. È inoltre costituito dal messaggio di suggerimento visualizzato sopra l’immagine statica.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS della vista principale**

L’aspetto della vista principale è controllato con il seguente selettore di classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview
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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo della vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la visualizzazione principale:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**Proprietà CSS del messaggio di suggerimento**

L’aspetto del messaggio di suggerimento è controllato con il seguente selettore di classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

È possibile configurare stile, dimensione, aspetto e offset verticale del font attraverso CSS. Tuttavia, l’allineamento orizzontale è gestito dalla logica del visualizzatore. Sovrascrittura tramite CSS utilizzando `left` o `right` proprietà non supportate.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Offset dal fondo della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nome carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura intorno al testo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di riempimento di sfondo del testo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raggio bordo </span> </p> </td> 
   <td colname="col2"> <p>Raggio del bordo di sfondo del testo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità </span> </p> </td> 
   <td colname="col2"> <p>Opacità di sfondo del testo del messaggio. </p> <p>Per Internet Explorer 8, utilizza <span class="codeph"> filtro:alfa(opacity-..) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Il messaggio di suggerimento può essere localizzato. Vedi [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) per ulteriori informazioni.

.

Esempio: per impostare un messaggio di suggerimento semitrasparente con un carattere bianco Arial® 12-px, uno scostamento di 50 pixel dal fondo della vista principale, della spaziatura e un bordo arrotondato:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```
