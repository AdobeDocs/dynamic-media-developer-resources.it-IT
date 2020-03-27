---
description: Lo strumento di condivisione Twitter è costituito da un pulsante aggiunto al pannello Condivisione social network. Quando un utente fa clic sul pulsante, viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social network. La posizione del pulsante è gestita completamente dallo strumento di condivisione mediante social network.
seo-description: Lo strumento di condivisione Twitter è costituito da un pulsante aggiunto al pannello Condivisione social network. Quando un utente fa clic sul pulsante, viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social network. La posizione del pulsante è gestita completamente dallo strumento di condivisione mediante social network.
seo-title: Condivisione Twitter
solution: Experience Manager
title: Condivisione Twitter
topic: Dynamic media
uuid: f5f1182f-f95c-43c4-b39f-1b50ed4a5458
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Condivisione Twitter{#twitter-share}

Lo strumento di condivisione Twitter è costituito da un pulsante aggiunto al pannello Condivisione social network. Quando un utente fa clic sul pulsante, viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social network. La posizione del pulsante è gestita completamente dallo strumento di condivisione mediante social network.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

L&#39;aspetto del pulsante Condivisione Twitter è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore `state` di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

È possibile rimuovere il pulsante dal pannello Condivisione social network impostando la proprietà `display:none` CSS della classe CSS.

La descrizione del pulsante può essere localizzata. Consultate [Localizzazione degli elementi](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)dell’interfaccia utente.

## Esempio {#section-5a8837ea208e48ed8dfa6a3c1a514492}

Per impostare un pulsante di condivisione Twitter di 28x28 pixel e visualizzare un’immagine diversa per ciascuno dei quattro stati del pulsante:

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

