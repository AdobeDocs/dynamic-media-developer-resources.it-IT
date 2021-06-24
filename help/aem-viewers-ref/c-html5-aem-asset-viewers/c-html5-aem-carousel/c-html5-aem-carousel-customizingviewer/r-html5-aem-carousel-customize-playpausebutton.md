---
description: Il pulsante Riproduci/Pausa consente all’utente di sospendere o riprendere il comportamento di riproduzione automatica carosello.
solution: Experience Manager
title: Pulsante PlayPause
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Developer,Business Practitioner
exl-id: 1b48aa7f-d1c8-4367-94c2-689991b90942
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 1%

---

# Pulsante PlayPause{#playpause-button}

Il pulsante Riproduci/Pausa consente all’utente di sospendere o riprendere il comportamento di riproduzione automatica carosello.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

Il pulsante è visibile solo se il parametro `CarouselViewer.autoplay` è impostato su `1`; altrimenti, è nascosto. È possibile ridimensionare, applicare uno skin e posizionare questo pulsante, rispetto alla barra di controllo che lo contiene, utilizzando CSS.

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto del pulsante è controllato con il seguente selettore di classe CSS:

`.s7carouselviewer .s7playpausebutton`

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
   <td colname="col2"> <p>Posizione dalla parte superiore del bordo del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posizione da destra del bordo del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sinistra  </span> </p> </td> 
   <td colname="col2"> <p>Posizione a sinistra del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal fondo del bordo del visualizzatore. </p> </td> 
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
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedere anche <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Spriti CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursore  </span> </p> </td> 
   <td colname="col2"> <p>Tipo di cursore. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md) .

Esempio: per impostare un pulsante di pausa di riproduzione di 28 x 28 pixel, che è posizionato 17 pixel dal fondo e 12 pixel dal bordo sinistro del visualizzatore, e che visualizza un’immagine diversa per ciascuno dei quattro stati del pulsante quando è selezionato o meno.

```
.s7carouselviewer .s7playpausebutton { 
bottom:17px; 
left:12px; 
width:28px; 
height:28px; 
} 
.s7carouselviewer .s7playpausebutton[selected='true'][state='up'] { 
  background-image:url(images/playBtn_up.png); 
} 
.s7carouselviewer .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/playBtn_over.png); 
} 
.s7carouselviewer .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/playBtn_down.png); 
} 
.s7carouselviewer .s7playpausebutton[selected='true'][state='disabled'] { 
background-image:url(images/playBtn_disabled.png); 
} 
.s7carouselviewer .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/pauseBtn_up.png); 
} 
.s7carouselviewer .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/pauseBtn_over.png); 
} 
.s7carouselviewer .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/pauseBtn_down.png); 
}
```
