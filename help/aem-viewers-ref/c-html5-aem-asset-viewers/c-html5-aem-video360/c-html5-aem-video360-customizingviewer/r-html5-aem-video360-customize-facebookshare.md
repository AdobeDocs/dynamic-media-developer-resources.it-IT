---
description: Lo strumento di condivisione Facebook è costituito da un pulsante aggiunto al pannello Condivisione social network. Quando un utente fa clic sul pulsante, viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social network. La posizione del pulsante è gestita completamente dallo strumento di condivisione mediante social network.
seo-description: Lo strumento di condivisione Facebook è costituito da un pulsante aggiunto al pannello Condivisione social network. Quando un utente fa clic sul pulsante, viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social network. La posizione del pulsante è gestita completamente dallo strumento di condivisione mediante social network.
seo-title: Condivisione Facebook
solution: Experience Manager
title: Condivisione Facebook
topic: Dynamic media
uuid: 8575fde4-4d03-4b87-a628-ff06ff8c91c9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Condivisione Facebook{#facebook-share}

Lo strumento di condivisione Facebook è costituito da un pulsante aggiunto al pannello Condivisione social network. Quando un utente fa clic sul pulsante, viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social network. La posizione del pulsante è gestita completamente dallo strumento di condivisione mediante social network.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

L&#39;aspetto del pulsante di condivisione Facebook è controllato dal seguente selettore di classe CSS:

```
.s7video360viewer .s7facebookshare
```

**Proprietà CSS dello strumento di condivisione Facebook**

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
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore `state` di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

È possibile rimuovere il pulsante dal pannello Condivisione social network impostando la proprietà `display:none` CSS della classe CSS.

La descrizione del pulsante può essere localizzata. Consultate [Localizzazione degli elementi](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)dell’interfaccia utente.

**Esempio** : per impostare un pulsante di condivisione Facebook di 28 x 28 pixel e visualizzare un’immagine diversa per ciascuno dei quattro stati del pulsante:

```
.s7video360viewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7video360viewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7video360viewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7video360viewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```

