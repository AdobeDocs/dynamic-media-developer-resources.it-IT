---
description: Toccando o facendo clic sul pulsante diapositiva successiva si sposta l’utente sulla diapositiva successiva del set di caroselli.
seo-description: Toccando o facendo clic sul pulsante diapositiva successiva si sposta l’utente sulla diapositiva successiva del set di caroselli.
seo-title: Diapositiva successiva
solution: Experience Manager
title: Diapositiva successiva
topic: Dynamic media
uuid: 6cf7a16c-42bf-4576-bcb1-d504589b2748
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Diapositiva successiva{#next-slide}

Toccando o facendo clic sul pulsante diapositiva successiva si sposta l’utente sulla diapositiva successiva del set di caroselli.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

Questo pulsante non viene visualizzato sui dispositivi touch. Potete ridimensionare, incarnato e posizionare questo pulsante tramite CSS.

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto del pulsante è controllato dal seguente selettore di classe CSS:

`.s7carouselviewer .s7panrightbutton`

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
   <td colname="col2"> <p>Posizione dalla parte superiore del bordo del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right </span> </p> </td> 
   <td colname="col2"> <p>Posizione da destra del bordo del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Posizione da sinistra del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Posizione nella parte inferiore del bordo del visualizzatore. </p> </td> 
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
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Vedere anche <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> cursor </span> </p> </td> 
   <td colname="col2"> <p>Tipo di cursore. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore `state` di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-localization.md) dell&#39;interfaccia utente.

Esempio: per impostare un pulsante di diapositiva precedente di 60 x 60 pixel, posizionato 10 pixel dal bordo destro del visualizzatore e centrato verticalmente, e visualizza un’immagine diversa per ciascuno dei quattro stati del pulsante.

```
.s7carouselviewer .s7panrightbutton{ 
 bottom: 50%; 
 right: 10px; 
 background-size:60px; 
 cursor: pointer; 
 } 
.s7carouselviewer.s7mouseinput .s7panrightbutton { 
 width:60px; 
 height:60px; 
 margin-bottom: -20px; 
} 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state]  { 
    background-image: url(../../viewers/s7viewers/html5/images/v2/CarouselDotsRightButton_dark_sprite.png); 
} 
 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state='up'] { background-position: -0px -60px;  } 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state='over'] { background-position: -0px -0px; } 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state='down'] { background-position: -0px -0px; } 
.s7carouselviewer.s7mouseinput .s7panrightbutton[state='disabled'] { background-position: -0px -60px; }
```

