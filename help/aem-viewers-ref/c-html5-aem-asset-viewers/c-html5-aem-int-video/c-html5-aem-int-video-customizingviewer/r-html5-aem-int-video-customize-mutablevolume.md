---
description: Il controllo del volume modificabile inizialmente viene visualizzato come un pulsante che consente all'utente di attivare o disattivare l'audio del lettore video.
seo-description: Il controllo del volume modificabile inizialmente viene visualizzato come un pulsante che consente all'utente di attivare o disattivare l'audio del lettore video.
seo-title: Volume variabile
solution: Experience Manager
title: Volume variabile
topic: Dynamic media
uuid: 3c3239ca-18fc-47ff-bc5d-2b50e1514e50
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Volume variabile{#mutable-volume}

Il controllo del volume modificabile inizialmente viene visualizzato come un pulsante che consente all&#39;utente di attivare o disattivare l&#39;audio del lettore video.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Quando un utente passa il mouse sul pulsante, viene visualizzato un cursore che consente all&#39;utente di impostare il volume. Il controllo del volume modificabile può essere ridimensionato, inclinato e posizionato, rispetto alla barra di controllo che lo contiene, tramite CSS.

L&#39;aspetto dell&#39;area del volume modificabile è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7mutablevolume
```

**Proprietà CSS del volume modificabile**

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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza del controllo del volume modificabile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del controllo del volume modificabile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Colore del controllo del volume mutabile. </p> </td> 
  </tr> 
 </tbody> 
</table>

L&#39;aspetto del pulsante Disattiva audio/Disattiva audio è controllato dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton
```

Potete controllare l&#39;immagine di sfondo per ogni stato del pulsante. Le dimensioni del pulsante vengono ereditate dalle dimensioni del controllo del volume.

**Proprietà CSS dell&#39;immagine pulsante**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta i selettori di attributi `state` e `selected`, che possono essere utilizzati per applicare interfacce diverse a stati di pulsante diversi. In particolare, `selected='true'` corrisponde allo stato &quot;muted&quot; e `selected='false'` corrisponde allo stato &quot;unmuted&quot;.

L&#39;area della barra del volume verticale è controllata dal seguente selettore di classe CSS:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume
```

**Proprietà CSS dell&#39;area della barra del volume verticale**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Larghezza del volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> Altezza del volume verticale. </p> </td> 
  </tr> 
 </tbody> 
</table>

La traccia all&#39;interno del controllo del volume verticale è controllata dai seguenti selettori di classe CSS:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**Proprietà CSS della traccia all&#39;interno del controllo del volume verticale**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del controllo del volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del controllo del volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altezza del controllo del volume verticale. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Grafica della manopola di controllo del volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della manopola di controllo del volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altezza della manopola di controllo del volume verticale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p>Posizione orizzontale della manopola di controllo del volume verticale. </p> </td> 
  </tr> 
 </tbody> 
</table>

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Esempi {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un pulsante di disattivazione audio che sia di 32 x 32 pixel e che sia posizionato 6 pixel dalla parte superiore, e di 38 pixel dal bordo destro della barra di controllo. Se selezionato o non selezionato, viene visualizzata un’immagine diversa per ciascuno dei quattro stati del pulsante.

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

Di seguito è riportato un esempio di come si può formattare il cursore del volume all&#39;interno del controllo del volume modificabile.

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

