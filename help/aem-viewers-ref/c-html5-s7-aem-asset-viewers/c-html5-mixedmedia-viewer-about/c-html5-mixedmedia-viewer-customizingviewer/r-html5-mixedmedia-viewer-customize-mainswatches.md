---
title: Campioni principali
description: I campioni principali sono costituiti da una riga di miniature con pulsanti di scorrimento opzionali sul lato sinistro e destro. I pulsanti di scorrimento sono visibili sul desktop solo se tutte le miniature non rientrano nella larghezza del contenitore. Sui dispositivi mobili o se le miniature possono rientrare nella larghezza del contenitore, i pulsanti di scorrimento non vengono visualizzati.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: e6ff32bf-f85a-4288-a0e5-34487229a9d9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 2%

---

# Campioni principali{#main-swatches}

I campioni principali sono costituiti da una riga di miniature con pulsanti di scorrimento opzionali sul lato sinistro e destro. I pulsanti di scorrimento sono visibili sul desktop solo se tutte le miniature non rientrano nella larghezza del contenitore. Sui dispositivi mobili o se le miniature possono rientrare nella larghezza del contenitore, i pulsanti di scorrimento non vengono visualizzati.

L’aspetto del contenitore campioni è controllato con il selettore di classe CSS:

```
.s7mixedmediaviewer .s7swatches
```

**Proprietà CSS dei campioni**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dei campioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Offset dei campioni verticali rispetto al contenitore del visualizzatore. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare campioni con altezza di 100 pixel.

```
.s7mixedmediviewer .s7swatches { 
 height: 100px;  
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

La spaziatura tra le miniature dei campioni è controllata dal seguente selettore di classe CSS:

`.s7mixedmediaviewer .s7swatches .s7thumbcell`

<table id="table_ECE063DB98154E099FB024F66FF877D7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p> La dimensione del margine orizzontale e verticale intorno a ciascuna miniatura. La spaziatura effettiva delle miniature è uguale alla somma dei margini sinistro e destro impostati per <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio**

Per impostare la spaziatura su dieci pixel sia in verticale che in orizzontale.

```
.s7mixedmediaviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

L’aspetto della singola miniatura viene controllato con il seguente selettore di classe CSS:

`.s7mixedmediaviewer .s7swatches .s7thumb`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Bordo della miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniatura supporta `state` selettore di attributi, che può essere utilizzato per applicare skin diversi a stati di miniature diversi. In particolare: `state="selected"` corrisponde alla miniatura dell&#39;immagine attualmente visualizzata nella visualizzazione principale, `state="default"` corrisponde al resto delle miniature, e `state="over"` al passaggio del mouse.

Esempio: per impostare miniature di 56 x 56 pixel, con un bordo predefinito grigio chiaro e un bordo selezionato grigio scuro.

```
.s7mixedmediaviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7mixedmediaviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7mixedviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

Il tipo di risorsa viene visualizzato come icona sopra l’immagine miniatura ed è controllato dal seguente selettore di classe CSS:

`.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay`

<table id="table_460FC57D12CC4B52B3782F4DFAC3A194"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della sovrapposizione icona. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della sovrapposizione icona. </p> </td> 
  </tr> 
 </tbody> 
</table>

La sovrapposizione supporta `type` selettore di attributi con i seguenti valori possibili: `image` (per immagini singole), `swatchset` (per i set di campioni), `spinset` (per i set 360 gradi) e `video` (per video singoli o set video adattivi).

Esempio: per impostare le sovrapposizioni di icone per set 360 gradi, set di campioni e video:

```
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="swatchset"] { 
 background-image: url(images/v2/ThumbOverlaySwatchSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="spinset"] { 
 background-image: url(images/v2/ThumbOverlaySpinSet.png);  
} 
.s7mixedmediaviewer .s7swatches .s7thumb .s7thumboverlay[type="video"] { 
 background-image: url(images/v2/ThumbOverlayVideo.png);  
}
```

L’aspetto dei pulsanti di scorrimento sinistro e destro è controllato dai seguenti selettori di classi CSS:

`.s7mixedmediaviewer .s7swatches .s7scrollleftbutton`

`.s7mixedmediaviewer .s7swatches .s7scrollrightbutton`

Non è possibile posizionare i pulsanti di scorrimento utilizzando CSS `top`, `left`, `bottom`, e `right` proprietà. Al contrario, la logica di visualizzazione li posiziona automaticamente.

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta `state` selettore di attributi, che può essere utilizzato per applicare skin diversi a stati di pulsante diversi: `up`, `down`, `over`, e `disabled`.

Le descrizioni dei pulsanti possono essere localizzate. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) per ulteriori informazioni.

Esempio: per impostare pulsanti di scorrimento di 56 x 56 pixel con grafica diversa per ogni stato.

```
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7mixedmediaviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```
