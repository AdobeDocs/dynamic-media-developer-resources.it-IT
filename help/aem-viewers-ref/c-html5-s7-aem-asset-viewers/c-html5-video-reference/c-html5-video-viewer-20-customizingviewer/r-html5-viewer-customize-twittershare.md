---
description: Lo strumento di condivisione Twitter è costituito da un pulsante aggiunto al pannello Condivisione social . Quando si fa clic sul pulsante, l'utente viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social. La posizione del pulsante è completamente gestita dallo strumento di condivisione social network.
solution: Experience Manager
title: Condividi su Twitter
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# Condivisione Twitter{#twitter-share}

Lo strumento di condivisione Twitter è costituito da un pulsante aggiunto al pannello Condivisione social . Quando si fa clic sul pulsante, l&#39;utente viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social. La posizione del pulsante è completamente gestita dallo strumento di condivisione social network.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

L&#39;aspetto del pulsante di condivisione Twitter è controllato con il seguente selettore di classe CSS:

```
.s7videoviewer .s7twittershare
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
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

È possibile rimuovere il pulsante dal pannello Condivisione social impostando la proprietà `display:none` CSS nella relativa classe CSS.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Esempio : per impostare un pulsante di condivisione Twitter di 28 x 28 pixel e visualizzare un’immagine diversa per ciascuno dei quattro stati diversi del pulsante:

```
.s7videoviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7videoviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7videoviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7videoviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```

