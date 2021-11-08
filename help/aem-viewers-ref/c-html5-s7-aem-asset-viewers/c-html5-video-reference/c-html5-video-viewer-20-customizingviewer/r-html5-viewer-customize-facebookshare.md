---
description: Facebook share tool consists of a button added to the Social share panel. When the button is selected the user is redirected to a sharing dialog box that is provided by a social service. La posizione del pulsante è completamente gestita dallo strumento di condivisione social network.
solution: Experience Manager
title: Facebook share
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 6b7e043f-6a9f-48ba-b811-3c94fe5c32f1
source-git-commit: fd3a1fe47da5ba26b53ea9414bfec1e4c11d7392
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---

# Facebook share{#facebook-share}

Facebook share tool consists of a button added to the Social share panel. Quando il pulsante è selezionato, l&#39;utente viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social. La posizione del pulsante è completamente gestita dallo strumento di condivisione social network.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

The appearance of the Facebook share button is controlled with the following CSS class selector:

```
.s7videoviewer .s7facebookshare
```

**CSS properties of the Facebook share tool**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>See <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta `state` selettore di attributi, che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

È possibile rimuovere il pulsante dal pannello Condivisione social impostando `display:none` Proprietà CSS nella relativa classe CSS.

The button tool tip can be localized. Vedi [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) per ulteriori informazioni.

Esempio: per impostare un pulsante di condivisione Facebook di 28 x 28 pixel e visualizzare un’immagine diversa per ciascuno dei quattro stati dei pulsanti:

```
.s7videoviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7videoviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7videoviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7videoviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
