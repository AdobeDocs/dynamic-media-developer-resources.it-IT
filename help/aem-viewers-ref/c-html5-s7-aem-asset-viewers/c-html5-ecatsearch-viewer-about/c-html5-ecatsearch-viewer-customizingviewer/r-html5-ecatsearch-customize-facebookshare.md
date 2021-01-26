---
description: Lo strumento di condivisione Facebook è costituito da un pulsante aggiunto al pannello Condivisione social network. Quando un utente fa clic sul pulsante, viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social network. La posizione del pulsante è gestita completamente dallo strumento di condivisione mediante social network.
seo-description: Lo strumento di condivisione Facebook è costituito da un pulsante aggiunto al pannello Condivisione social network. Quando un utente fa clic sul pulsante, viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social network. La posizione del pulsante è gestita completamente dallo strumento di condivisione mediante social network.
seo-title: Condivisione Facebook
solution: Experience Manager
title: Condivisione Facebook
topic: Dynamic Media
uuid: 1b79ad43-7fdf-4046-a225-1f585ff839b6
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# Condivisione Facebook{#facebook-share}

Lo strumento di condivisione Facebook è costituito da un pulsante aggiunto al pannello Condivisione social network. Quando un utente fa clic sul pulsante, viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social network. La posizione del pulsante è gestita completamente dallo strumento di condivisione mediante social network.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

L&#39;aspetto del pulsante di condivisione Facebook è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7facebookshare
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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

È possibile rimuovere il pulsante dal pannello Condivisione social network impostando la proprietà CSS `display:none` nella classe CSS corrispondente.

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Esempio: per impostare un pulsante di condivisione Facebook di 28x28 pixel e visualizzare un’immagine diversa per ciascuno dei quattro stati del pulsante:

```
.s7ecatalogsearchviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```

