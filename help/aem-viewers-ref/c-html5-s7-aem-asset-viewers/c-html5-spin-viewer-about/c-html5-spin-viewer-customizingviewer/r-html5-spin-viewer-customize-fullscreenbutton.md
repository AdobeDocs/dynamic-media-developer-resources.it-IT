---
description: Questo pulsante consente al visualizzatore di entrare o uscire dalla modalità a schermo intero quando l’utente fa clic su di esso. Questo pulsante non viene visualizzato se il visualizzatore funziona in modalità pop-up e il sistema non supporta lo schermo intero nativo. Questo pulsante può essere ridimensionato, incarnato e posizionato mediante CSS.
seo-description: Questo pulsante consente al visualizzatore di entrare o uscire dalla modalità a schermo intero quando l’utente fa clic su di esso. Questo pulsante non viene visualizzato se il visualizzatore funziona in modalità pop-up e il sistema non supporta lo schermo intero nativo. Questo pulsante può essere ridimensionato, incarnato e posizionato mediante CSS.
seo-title: Pulsante Schermo intero
solution: Experience Manager
title: Pulsante Schermo intero
topic: Dynamic media
uuid: 22d10ec1-83f3-4f86-a0a1-0fc2e43232b1
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Full screen button{#full-screen-button}

Questo pulsante consente al visualizzatore di entrare o uscire dalla modalità a schermo intero quando l’utente fa clic su di esso. Questo pulsante non viene visualizzato se il visualizzatore funziona in modalità pop-up e il sistema non supporta lo schermo intero nativo. Questo pulsante può essere ridimensionato, incarnato e posizionato mediante CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto del pulsante è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
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
   <td colname="col2"> <p>Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta sia i selettori `state` che gli `selected` attributi, che possono essere utilizzati per applicare interfacce diverse a diversi stati del pulsante. In particolare, `selected='true'` corrisponde allo stato &quot;a schermo intero&quot; e `selected='false'` allo stato &quot;normale&quot;.

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98) dell&#39;interfaccia utente.

Esempio: per impostare un pulsante a schermo intero di 32 x 32 pixel, posizionato sei pixel dal bordo superiore e destro del visualizzatore e, se selezionato o meno, visualizza un’immagine diversa per ciascuno dei quattro stati del pulsante:

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

