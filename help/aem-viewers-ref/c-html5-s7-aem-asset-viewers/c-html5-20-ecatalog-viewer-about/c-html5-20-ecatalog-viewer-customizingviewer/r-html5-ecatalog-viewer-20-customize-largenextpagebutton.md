---
description: Tocca o fai clic su questo pulsante per passare alla pagina successiva del catalogo. Questo pulsante viene visualizzato nella barra di controllo principale. Questo pulsante non viene visualizzato sui telefoni cellulari per risparmiare spazio su schermo. Puoi ridimensionare, skin e posizionare questo pulsante utilizzando CSS.
solution: Experience Manager
title: Pulsante Pagina successiva grande
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Developer,User
exl-id: 8147cdf8-298c-4713-a5a5-b34674f6b2c8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---

# Pulsante Pagina successiva grande{#large-next-page-button}

Tocca o fai clic su questo pulsante per passare alla pagina successiva del catalogo. Questo pulsante viene visualizzato nella barra di controllo principale. Questo pulsante non viene visualizzato sui telefoni cellulari per risparmiare spazio su schermo. Puoi ridimensionare, skin e posizionare questo pulsante utilizzando CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto del pulsante è controllato con il seguente selettore di classe CSS:

`.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton`

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
   <td colname="col2"> <p>Posizione dal bordo superiore della barra di controllo principale, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo destro della barra di controllo principale, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sinistra  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo sinistro della barra di controllo principale, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo inferiore della barra di controllo principale, compresa la spaziatura. </p> </td> 
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

Esempio: per impostare un grande pulsante per la pagina successiva di 56 x 56 pixel, centrato verticalmente e ancorato al bordo destro del visualizzatore, e visualizza un’immagine diversa per ciascuno dei quattro stati del pulsante.

```
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton { 
bottom:50%; 
margin-bottom:-28px; 
right:0px; 
width:56px; 
height:56px; 
} 
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/RightButton_dark_up.png); 
} 
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/RightButton_dark_over.png); 
} 
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/RightButton_dark_down.png); 
} 
.s7ecatalogviewer .s7ecatrightbutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/RightButton_dark_disabled.png); 
}
```
