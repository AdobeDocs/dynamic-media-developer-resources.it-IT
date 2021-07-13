---
description: Lo strumento di condivisione twitter è costituito da un pulsante aggiunto al pannello Condivisione social. Quando si fa clic sul pulsante, l'utente viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social. La posizione del pulsante è completamente gestita dallo strumento di condivisione social network.
solution: Experience Manager
title: Condivisione twitter
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Developer,User
exl-id: 045ca718-b971-4437-a0bf-580eee83ff2d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 1%

---

# Condivisione twitter{#twitter-share}

Lo strumento di condivisione twitter è costituito da un pulsante aggiunto al pannello Condivisione social. Quando si fa clic sul pulsante, l&#39;utente viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social. La posizione del pulsante è completamente gestita dallo strumento di condivisione social network.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

L&#39;aspetto del pulsante di condivisione Twitter è controllato con il seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7twittershare
```

**Proprietà CSS dello strumento di condivisione Twitter**

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
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

È possibile rimuovere il pulsante dal pannello Condivisione social impostando la proprietà `display:none` CSS nella relativa classe CSS.

La descrizione comando del pulsante può essere localizzata. Consulta [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Esempio {#section-5a8837ea208e48ed8dfa6a3c1a514492}

Per impostare un pulsante di condivisione Twitter di 28 x 28 pixel e visualizzare un’immagine diversa per ciascuno dei quattro stati del pulsante:

```
.s7interactivevideoviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7interactivevideoviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7interactivevideoviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7interactivevideoviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7interactivevideoviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
