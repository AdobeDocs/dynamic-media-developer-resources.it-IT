---
title: Condividi su Twitter
description: Lo strumento di condivisione Twitter è costituito da un pulsante aggiunto al pannello Condivisione social. Quando il pulsante è selezionato, l’utente viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social. La posizione del pulsante è completamente gestita dallo strumento Condivisione social.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 1db2600d-d13f-4563-b40a-098485e0ddf9
TQID: 'https://experienceleague.adobe.com/kI5nf54HbIlIa0puL0-PD-yX54psYCOWtnuGk7n8Ukw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 0%

---

# Condividi su Twitter{#twitter-share}

Lo strumento di condivisione Twitter è costituito da un pulsante aggiunto al pannello Condivisione social. Quando il pulsante è selezionato, l’utente viene reindirizzato a una finestra di dialogo di condivisione fornita da un servizio social. La posizione del pulsante è completamente gestita dallo strumento Condivisione social.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

L’aspetto del pulsante di condivisione Twitter è controllato dal seguente selettore di classe CSS:

```
.s7videoviewer .s7twittershare
```

**Proprietà CSS dello strumento di condivisione Twitter**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedere <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse a diversi stati di pulsante.

È possibile rimuovere il pulsante dal pannello Condivisione social impostando la proprietà CSS `display:none` sulla relativa classe CSS.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

Esempio: per impostare un pulsante di condivisione Twitter di 28 x 28 pixel e visualizzare un&#39;immagine diversa per ciascuno dei quattro stati dei pulsanti:

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
