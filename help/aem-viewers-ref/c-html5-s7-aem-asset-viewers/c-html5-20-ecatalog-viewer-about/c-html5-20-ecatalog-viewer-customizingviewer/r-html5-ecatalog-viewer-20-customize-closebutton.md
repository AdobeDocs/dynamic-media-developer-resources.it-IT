---
title: Chiudi pulsante
description: Selezionando o toccando questo pulsante si chiude la pagina Web contenitore. Questo pulsante viene visualizzato solo se il parametro closebutton è impostato su 1. Questo pulsante non è disponibile nei sistemi desktop. Potete ridimensionare, interfacciare e posizionare questo pulsante utilizzando i CSS.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 07dc3a95-1f3e-44c4-8126-621f10aec212
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Chiudi pulsante{#close-button}

Selezionando o toccando questo pulsante si chiude la pagina Web contenitore. Questo pulsante viene visualizzato solo se il parametro closebutton è impostato su 1. Questo pulsante non è disponibile nei sistemi desktop. Potete ridimensionare, interfacciare e posizionare questo pulsante utilizzando i CSS.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L&#39;aspetto del pulsante è controllato con i seguenti selettore di classe CSS:

`.s7ecatalogviewer .s7closebutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> In alto </span> </p> </td> 
   <td colname="col2"> <p>Posizione dalla parte superiore bordo della barra di controllo principale, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A destra </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro della barra di controllo principale, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A sinistra </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo sinistro della barra di controllo principale, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Fondoschiena </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo inferiore della barra di controllo principale, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per uno stato pulsante specificato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all'interno dello sprite dell'illustrazione, se vengono utilizzati sprite CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo supporta pulsante il `state` selettore attributo, che potete utilizzare per applicare interfacce diverse a diversi stati pulsante.

Il suggerimento strumento pulsante può essere localizzato. Per ulteriori informazioni, consulta [Localizzazione di utente elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) dell&#39;interfaccia.

Esempio: per impostare un Chiudi pulsante di 56 x 56 pixel posizionato a 4 pixel dal bordo superiore e destro della barra di controllo principale. Infine, visualizza un&#39;immagine diversa per ciascuno dei quattro diversi stati pulsante.

```
.s7ecatalogviewer .s7closebutton { 
top:4px; 
right:4px; 
width:56px; 
height:56px; 
} 
.s7ecatalogviewer .s7closebutton [state='up'] { 
background-image:url(images/v2/CloseButton_dark_up.png); 
} 
.s7ecatalogviewer .s7closebutton [state='over'] {  
background-image:url(images/v2/CloseButton_dark_over.png); 
} 
.s7ecatalogviewer .s7closebutton [state='down'] {  
background-image:url(images/v2/CloseButton_dark_down.png); 
} 
.s7ecatalogviewer .s7closebutton [state='disabled'] { 
background-image:url(images/v2/CloseButton_dark_disabled.png); 
}
```
