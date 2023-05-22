---
title: Volume variabile
description: Il controllo del volume mutabile viene inizialmente visualizzato come un pulsante che consente all'utente di disattivare o attivare l'audio del lettore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: ecef47c1-e659-4930-bfb1-cc5e7c059094
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---

# Volume variabile{#mutable-volume}

Il controllo del volume mutabile viene inizialmente visualizzato come un pulsante che consente all&#39;utente di disattivare o attivare l&#39;audio del lettore video.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Quando un utente passa il mouse sul pulsante, viene visualizzato un cursore che consente di impostare il volume. Il controllo volume modificabile può essere ridimensionato, interpolato e posizionato in base alla barra di controllo che lo contiene tramite CSS.

L’aspetto dell’area del volume mutabile è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7mutablevolume
```

**Proprietà CSS del volume modificabile**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> destra </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo destro, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza del controllo volume modificabile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del controllo volume modificabile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore del controllo volume modificabile. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’aspetto del pulsante di disattivazione audio/attivazione audio è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton
```

È possibile controllare l&#39;immagine di sfondo per ogni stato del pulsante. Le dimensioni del pulsante vengono ereditate dalle dimensioni del controllo volume.

**Proprietà CSS dell’immagine del pulsante**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Consulta <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta sia `state` e `selected` selettori di attributi, che possono essere utilizzati per applicare interfacce diverse a stati di pulsante diversi. In particolare: `selected='true'` corrisponde allo stato &quot;disattivato&quot; e `selected='false'` corrisponde allo stato &quot;unmuted&quot;.

L’area verticale della barra del volume è controllata con il seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume
```

**Proprietà CSS dell&#39;area verticale della barra del volume**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza del volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Altezza del volume verticale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il tracciamento all&#39;interno del controllo del volume verticale è controllato con i seguenti selettori di classe CSS:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**Proprietà CSS del brano all&#39;interno del controllo volume verticale**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del controllo volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del controllo volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del controllo volume verticale. </p> </td> 
  </tr> 
 </tbody> 
</table>

La manopola del volume verticale è controllata con il seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**Proprietà CSS della manopola di controllo del volume verticale**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Illustrazione della manopola di controllo del volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Consulta <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della manopola di controllo del volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della manopola di controllo del volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Posizione orizzontale della manopola di controllo del volume verticale. </p> </td> 
  </tr> 
 </tbody> 
</table>

La descrizione comando del pulsante può essere localizzata. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

## Esempi {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un pulsante di disattivazione audio di 32 x 32 pixel posizionato a 6 pixel dall&#39;alto e a 38 pixel dal bordo destro della barra di controllo. Visualizzare un&#39;immagine diversa per ciascuno dei quattro diversi stati dei pulsanti, se selezionato o meno.

```
.s7interactivevideoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

Di seguito è riportato un esempio di come applicare uno stile al cursore del volume all&#39;interno del controllo volume modificabile.

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```
