---
description: Tocca o fai clic su questo pulsante per ingrandire un’immagine nella vista principale. Questo pulsante non viene visualizzato sui telefoni cellulari al fine di salvare lo schermo immobiliare. Puoi ridimensionare, skin e posizionare questo pulsante utilizzando CSS.
solution: Experience Manager
title: Pulsante Zoom out
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Zoom
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 1%

---


# Pulsante Zoom out{#zoom-out-button}

Tocca o fai clic su questo pulsante per ingrandire un’immagine nella vista principale. Questo pulsante non viene visualizzato sui telefoni cellulari al fine di salvare lo schermo immobiliare. Puoi ridimensionare, skin e posizionare questo pulsante utilizzando CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto del pulsante è controllato con il seguente selettore di classe CSS:

```
.s7basiczoomviewer .s7zoomoutbutton
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
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sinistra  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo sinistro, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-customizingviewer/c-html5-20-basic-zoom-viewer-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Esempio: per impostare un pulsante di zoom out di 32 x 32 pixel, posizionato sei pixel dal bordo superiore e destro del visualizzatore, e visualizza un’immagine diversa per ciascuno dei quattro stati dei pulsanti.

```
.s7basiczoomviewer .s7zoomoutbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7basiczoomviewer .s7zoomoutbutton [state='up'] { 
background-image:url(images/v2/ZoomOutButton_dark_up.png); 
} 
.s7basiczoomviewer .s7zoomoutbutton [state='over'] {  
background-image:url(images/v2/ZoomOutButton_dark_over.png); 
} 
.s7basiczoomviewer .s7zoomoutbutton [state='down'] {  
background-image:url(images/v2/ZoomOutButton_dark_down.png); 
} 
.s7basiczoomviewer .s7zoomoutbutton [state='disabled'] { 
background-image:url(images/v2/ZoomOutButton_dark_disabled.png); 
}
```

