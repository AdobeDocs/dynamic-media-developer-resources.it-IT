---
description: Questo pulsante attiva e disattiva la visualizzazione della didascalia chiusa. Non è visibile se il parametro caption non è specificato.
seo-description: Questo pulsante attiva e disattiva la visualizzazione della didascalia chiusa. Non è visibile se il parametro caption non è specificato.
seo-title: Pulsante Didascalia
solution: Experience Manager
title: Pulsante Didascalia
topic: Dynamic media
uuid: 97de8cdd-8410-4128-be5c-1fc4987a5f96
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%

---


# Pulsante Didascalia{#caption-button}

Questo pulsante attiva e disattiva la visualizzazione della didascalia chiusa. Non è visibile se il parametro caption non è specificato.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Utilizzando CSS potete ridimensionare, applicare l&#39;interfaccia e posizionare il pulsante in relazione alla barra di controllo che lo contiene.

L&#39;aspetto di questo pulsante è controllato dal seguente selettore di classe CSS:

```
.s7videoviewer .s7closedcaptionbutton
```

**Proprietà CSS del pulsante didascalia**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo destro, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo sinistro, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal bordo inferiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza del pulsante a schermo intero. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante a schermo intero. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta i selettori di attributi `state` e `selected`, che possono essere utilizzati per applicare interfacce diverse a stati di pulsante diversi. In particolare, `selected='true'` corrisponde allo stato in cui le didascalie sono visibili e `selected='false'` viene utilizzato quando le didascalie sono nascoste.

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un pulsante per sottotitoli codificati di 28x28 pixel, posizionati quattro pixel dalla parte superiore e 68 pixel dal bordo destro della barra di controllo, e visualizza un’immagine diversa per ciascuno dei quattro stati del pulsante, se selezionato o meno.

```
.s7videoviewer .s7closedcaptionbutton { 
 position:absolute; 
 top:4px; 
 right:68px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7closedcaptionbutton[selected='true'][state='up'] { 
background-image:url(images/v2/ClosedCaptionButton_up.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='true'][state='over'] { 
background-image:url(images/v2/ClosedCaptionButton_over.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='true'][state='down'] { 
background-image:url(images/v2/ClosedCaptionButton_down.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='false'][state='up'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='false'][state='over'] { 
background-image:url(images/v2/ClosedCaptionButton_over.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='false'][state='down'] { 
background-image:url(images/v2/ClosedCaptionButton_down.png); 
} 
.s7videoviewer .s7closedcaptionbutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/ClosedCaptionButton_disabled.png);  
}
```

