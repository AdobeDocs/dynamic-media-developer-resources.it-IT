---
description: Toccando o facendo clic su questo pulsante si esegue lo zoom out su un’immagine nella vista principale. Questo pulsante non viene visualizzato sui telefoni cellulari per risparmiare spazio sullo schermo. Questo pulsante può essere ridimensionato, incarnato e posizionato mediante CSS.
seo-description: Toccando o facendo clic su questo pulsante si esegue lo zoom out su un’immagine nella vista principale. Questo pulsante non viene visualizzato sui telefoni cellulari per risparmiare spazio sullo schermo. Questo pulsante può essere ridimensionato, incarnato e posizionato mediante CSS.
seo-title: Pulsante Zoom out
solution: Experience Manager
title: Pulsante Zoom out
topic: Dynamic media
uuid: cf1c62eb-e0a4-413d-93d3-3aed31e9a444
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Zoom out button{#zoom-out-button}

Toccando o facendo clic su questo pulsante si esegue lo zoom out su un’immagine nella vista principale. Questo pulsante non viene visualizzato sui telefoni cellulari per risparmiare spazio sullo schermo. Questo pulsante può essere ridimensionato, incarnato e posizionato mediante CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto del pulsante è controllato dal seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7zoomoutbutton`

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
   <td colname="col2"> <p>Posizione dal bordo superiore della barra di controllo principale, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro della barra di controllo principale, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo sinistro della barra di controllo principale, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo inferiore della barra di controllo principale, inclusa la spaziatura. </p> </td> 
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
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore `state` di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) dell&#39;interfaccia utente.

Esempio: per impostare un pulsante di zoom out di 28 x 28 pixel, posizionato 4 pixel dal basso e 75 pixel dal bordo destro della barra di controllo principale, e visualizza un’immagine diversa per ciascuno dei quattro stati del pulsante.

```
.s7ecatalogsearchviewer .s7zoomoutbutton { 
bottom:4px; 
right:75px; 
width:28px; 
height:28px; 
} 
.s7ecatalogsearchviewer .s7zoomoutbutton [state='up'] { 
background-image:url(images/v2/ZoomOutButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7zoomoutbutton [state='over'] {  
background-image:url(images/v2/ZoomOutButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7zoomoutbutton [state='down'] {  
background-image:url(images/v2/ZoomOutButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7zoomoutbutton [state='disabled'] { 
background-image:url(images/v2/ZoomOutButton_dark_disabled.png); 
}
```

