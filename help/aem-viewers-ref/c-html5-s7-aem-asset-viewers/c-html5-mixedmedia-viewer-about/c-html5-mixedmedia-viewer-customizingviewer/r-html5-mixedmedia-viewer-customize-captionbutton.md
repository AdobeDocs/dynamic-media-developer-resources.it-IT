---
title: Pulsante Didascalia
description: Attiva e disattiva la visualizzazione dei sottotitoli. Non è visibile se il parametro della didascalia non è specificato. È possibile utilizzare CSS per ridimensionare, skin e posizionare questo pulsante rispetto alla barra di controllo che lo contiene.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 62809036-f158-402d-a8b2-2b9335e8c079
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---

# Pulsante Didascalia{#caption-button}

Attiva e disattiva la visualizzazione dei sottotitoli. Non è visibile se il parametro della didascalia non è specificato. È possibile utilizzare CSS per ridimensionare, skin e posizionare questo pulsante rispetto alla barra di controllo che lo contiene.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto del pulsante è controllato con il seguente selettore di classe CSS:

```
.s7mixedmediaviewer .s7closedcaptionbutton
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
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sinistra </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo sinistro, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo inferiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta `state` selettore di attributi e selettori di attributi selezionati, che possono essere utilizzati per applicare interfacce diverse a diversi stati dei pulsanti. In particolare, `selected='true'` corrisponde allo stato in cui le didascalie sono visibili e `selected='false'` viene utilizzato quando le didascalie sono nascoste.

La descrizione comando del pulsante può essere localizzata. Vedi [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) per ulteriori informazioni.

Esempio: per impostare un pulsante per sottotitoli codificati pari a 28 x 28 pixel, posizionato quattro pixel dalla parte superiore e 68 pixel dal bordo destro della barra di controllo. Infine, visualizza un’immagine diversa per ciascuno dei quattro stati dei pulsanti selezionati o meno.

```
.s7mixedmediaviewer .s7closedcaptionbutton { 
 position:absolute; 
 top:4px; 
 right:68px; 
 width:28px; 
 height:28px; 
} 
.s7mixedmediaviewer .s7closedcaptionbutton[selected='true'][state='up'] { 
background-image:url(images/v2/ClosedCaptionButton_up.png); 
} 
.s7mixedmediaviewer .s7closedcaptionbutton[selected='true'][state='over'] { 
background-image:url(images/v2/ClosedCaptionButton_over.png); 
} 
.s7mixedmediaviewer .s7closedcaptionbutton[selected='true'][state='down'] { 
background-image:url(images/v2/ClosedCaptionButton_down.png); 
} 
.s7mixedmediaviewer .s7closedcaptionbutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png); 
} 
.s7mixedmediaviewer .s7closedcaptionbutton[selected='false'][state='up'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png); 
} 
.s7mixedmediaviewer .s7closedcaptionbutton[selected='false'][state='over'] { 
background-image:url(images/v2/ClosedCaptionButton_over.png); 
} 
.s7mixedmediaviewer .s7closedcaptionbutton[selected='false'][state='down'] { 
background-image:url(images/v2/ClosedCaptionButton_down.png); 
} 
.s7mixedmediaviewer .s7closedcaptionbutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png);  
}
```
