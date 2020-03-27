---
description: Il pulsante a schermo intero consente al visualizzatore di entrare o uscire dalla modalità a schermo intero quando l’utente fa clic su di esso. Viene usato quando il visualizzatore visualizza il video e si trova nella barra di controllo. Questo pulsante non viene visualizzato se il visualizzatore funziona in modalità pop-up e il sistema non supporta lo schermo intero nativo.
seo-description: Il pulsante a schermo intero consente al visualizzatore di entrare o uscire dalla modalità a schermo intero quando l’utente fa clic su di esso. Viene usato quando il visualizzatore visualizza il video e si trova nella barra di controllo. Questo pulsante non viene visualizzato se il visualizzatore funziona in modalità pop-up e il sistema non supporta lo schermo intero nativo.
seo-title: Video, pulsante a schermo intero
solution: Experience Manager
title: Video, pulsante a schermo intero
topic: Dynamic media
uuid: f264154b-eb4d-4dcb-b8c0-e06c383198ae
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video, pulsante a schermo intero{#video-full-screen-button}

Il pulsante a schermo intero consente al visualizzatore di entrare o uscire dalla modalità a schermo intero quando l’utente fa clic su di esso. Viene usato quando il visualizzatore visualizza il video e si trova nella barra di controllo. Questo pulsante non viene visualizzato se il visualizzatore funziona in modalità pop-up e il sistema non supporta lo schermo intero nativo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Per CSS potete ridimensionare, applicare l&#39;interfaccia e posizionare il pulsante a schermo intero, rispetto alla barra di controllo che lo contiene.

L&#39;aspetto del pulsante a schermo intero è controllato dal selettore di classe CSS:

```
.s7mixedmediaviewer .s7fullscreenbutton
```

**Proprietà CSS del pulsante a schermo intero**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo destro, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo sinistro, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo inferiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza del pulsante a schermo intero. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante a schermo intero. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta sia i selettori `state` che gli `selected` attributi, che possono essere utilizzati per applicare interfacce diverse a diversi stati del pulsante. In particolare, `selected='true'` corrisponde allo stato &quot;a schermo intero&quot; e `selected='false'` allo stato &quot;normale&quot;.

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) dell&#39;interfaccia utente.

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un pulsante a schermo intero di 32 x 32 pixel e posizionato 6 pixel dal bordo superiore e destro della barra di controllo. Inoltre, quando selezionato o non selezionato, viene visualizzata un’immagine diversa per ciascuno dei quattro stati del pulsante.

```
.s7mixedmediaviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```

