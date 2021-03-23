---
description: Tocca o fai clic su questo pulsante per ripristinare un’immagine nella vista principale. Questo pulsante viene visualizzato nella barra di controllo principale sui sistemi desktop e sui tablet. Sui telefoni cellulari, questo pulsante appare nel centro in basso sopra l'immagine. Tuttavia, non viene visualizzato quando l'immagine è in uno stato di ripristino. Puoi ridimensionare, skin e posizionare questo pulsante utilizzando CSS.
seo-description: Tocca o fai clic su questo pulsante per ripristinare un’immagine nella vista principale. Questo pulsante viene visualizzato nella barra di controllo principale sui sistemi desktop e sui tablet. Sui telefoni cellulari, questo pulsante appare nel centro in basso sopra l'immagine. Tuttavia, non viene visualizzato quando l'immagine è in uno stato di ripristino. Puoi ridimensionare, skin e posizionare questo pulsante utilizzando CSS.
seo-title: Pulsante Ripristina zoom
solution: Experience Manager
title: Pulsante Ripristina zoom
uuid: 27f6eacd-2922-4ddb-98e4-ee10d3b72b0c
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# Pulsante di ripristino dello zoom{#zoom-reset-button}

Tocca o fai clic su questo pulsante per ripristinare un’immagine nella vista principale. Questo pulsante viene visualizzato nella barra di controllo principale sui sistemi desktop e sui tablet. Sui telefoni cellulari, questo pulsante appare nel centro in basso sopra l&#39;immagine. Tuttavia, non viene visualizzato quando l&#39;immagine è in uno stato di ripristino. Puoi ridimensionare, skin e posizionare questo pulsante utilizzando CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto del pulsante è controllato con il seguente selettore di classe CSS:

`.s7ecatalogviewer .s7zoomresetbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore della barra di controllo principale (su desktop e tablet) o del visualizzatore (su telefoni cellulari), compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro della barra di controllo principale (su desktop e tablet) o del visualizzatore (su telefoni cellulari), compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sinistra  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo sinistro della barra di controllo principale (su desktop e tablet) o del visualizzatore (su telefoni cellulari), compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo inferiore della barra di controllo principale (su desktop e tablet) o del visualizzatore (su telefoni cellulari), compresa la spaziatura. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Esempio: per impostare un pulsante di ripristino dello zoom di 28 x 28 pixel, posizionato (sul desktop) a 4 pixel dal fondo e a 47 pixel dal bordo destro della barra di controllo principale, e visualizza un’immagine diversa per ciascuno dei quattro stati del pulsante.

```
.s7ecatalogviewer .s7zoomresetbutton { 
bottom:4px; 
right:47px; 
width:28px; 
height:28px; 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='up'] { 
background-image:url(images/v2/ZoomResetButton_dark_up.png); 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='over'] {  
background-image:url(images/v2/ZoomResettButton_dark_over.png); 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='down'] {  
background-image:url(images/v2/ZoomResetButton_dark_down.png); 
} 
.s7ecatalogviewer .s7zoomresetbutton [state='disabled'] { 
background-image:url(images/v2/ZoomResetButton_dark_disabled.png); 
}
```

