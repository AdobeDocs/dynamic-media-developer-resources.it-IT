---
title: pulsante a schermo intero
description: Questo pulsante consente al visualizzatore di entrare o uscire dalla modalità a schermo intero quando viene selezionato dall’utente. Questo pulsante non viene visualizzato se il visualizzatore funziona in modalità pop-up e il sistema non supporta la modalità nativa a schermo intero. Puoi ridimensionare, applicare lo skin e posizionare questo pulsante utilizzando gli stili CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: c57f42e1-93c0-44fa-9734-9599786ee246
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 1%

---

# pulsante a schermo intero{#full-screen-button}

Questo pulsante consente al visualizzatore di entrare o uscire dalla modalità a schermo intero quando viene selezionato dall’utente. Questo pulsante non viene visualizzato se il visualizzatore funziona in modalità pop-up e il sistema non supporta la modalità nativa a schermo intero. Puoi ridimensionare, applicare lo skin e posizionare questo pulsante utilizzando gli stili CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto del pulsante è controllato dal seguente selettore di classe CSS:

```
.s7spinviewer .s7fullscreenbutton
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
   <td colname="col1"> <p> <span class="codeph"> destra </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta sia `state` e `selected` selettori di attributi, che possono essere utilizzati per applicare interfacce diverse a stati di pulsante diversi. In particolare: `selected='true'` corrisponde allo stato &quot;schermo intero&quot; e `selected='false'` corrisponde allo stato &quot;normale&quot;.

La descrizione comando del pulsante può essere localizzata. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98) per ulteriori informazioni.

Esempio: per impostare un pulsante a schermo intero di 32 x 32 pixel e posizionare sei pixel dal bordo superiore e destro del visualizzatore. Infine, visualizza un&#39;immagine diversa per ciascuno dei quattro diversi stati del pulsante, se selezionato o meno:

```
.s7spinviewer .s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7spinviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7spinviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7spinviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7spinviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7spinviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7spinviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7spinviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7spinviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```
