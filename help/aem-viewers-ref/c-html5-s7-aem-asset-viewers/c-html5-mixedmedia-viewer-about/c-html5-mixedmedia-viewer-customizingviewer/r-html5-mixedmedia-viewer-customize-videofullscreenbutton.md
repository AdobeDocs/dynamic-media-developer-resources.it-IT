---
description: Il pulsante a schermo intero consente al visualizzatore di entrare o uscire dalla modalità a schermo intero quando l’utente fa clic su di esso. Viene utilizzato quando il visualizzatore visualizza video e si trova nella barra di controllo. Questo pulsante non viene visualizzato se il visualizzatore funziona in modalità pop-up e il sistema non supporta lo schermo intero nativo.
solution: Experience Manager
title: Pulsante a schermo intero video
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: 45811efa-95f6-4b6d-96f8-9e5437a55f0e
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# Pulsante a schermo intero video{#video-full-screen-button}

Il pulsante a schermo intero consente al visualizzatore di entrare o uscire dalla modalità a schermo intero quando l’utente fa clic su di esso. Viene utilizzato quando il visualizzatore visualizza video e si trova nella barra di controllo. Questo pulsante non viene visualizzato se il visualizzatore funziona in modalità pop-up e il sistema non supporta lo schermo intero nativo.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

È possibile ridimensionare, applicare uno skin e posizionare il pulsante a schermo intero, in relazione alla barra di controllo che lo contiene, tramite CSS.

L’aspetto del pulsante a schermo intero è controllato con il selettore di classe CSS:

```
.s7mixedmediaviewer .s7fullscreenbutton
```

**Proprietà CSS del pulsante a schermo intero**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo superiore, inclusa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> Posizione dal bordo destro, compresa la spaziatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sinistra  </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta sia i selettori di attributi `state` che `selected` , che possono essere utilizzati per applicare interfacce diverse a diversi stati dei pulsanti. In particolare, `selected='true'` corrisponde allo stato &quot;a schermo intero&quot; e `selected='false'` corrisponde allo stato &quot;normale&quot;.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) .

## Esempio {#section-e8caea0a303c425a8a637c2a47c06355}

Per impostare un pulsante a schermo intero di 32 x 32 pixel e posizionato 6 pixel dal bordo superiore e destro della barra di controllo. Inoltre, se selezionato o non selezionato, mostra un’immagine diversa per ciascuno dei quattro stati del pulsante.

```
.s7mixedmediaviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```
