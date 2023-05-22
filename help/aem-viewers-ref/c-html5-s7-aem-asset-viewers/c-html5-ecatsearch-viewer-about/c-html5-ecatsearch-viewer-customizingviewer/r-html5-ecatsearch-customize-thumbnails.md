---
title: Miniature
description: Le miniature sono costituite da una griglia di miniature con una barra di scorrimento opzionale sul lato destro per consentire lo scorrimento verticale.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 25032917-237c-4227-92bd-ce66a6d003a0
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 1%

---

# Miniature{#thumbnails}

Le miniature sono costituite da una griglia di miniature con una barra di scorrimento opzionale sul lato destro per consentire lo scorrimento verticale.

Per attivare o disattivare le miniature, fai clic sul pulsante delle miniature nella barra di controllo principale. Quando le miniature sono attive, vengono visualizzate in modalità modale sovrapposta all’interfaccia utente del visualizzatore. La logica di visualizzazione ridimensiona automaticamente il contenitore delle miniature sull’intera area di visualizzazione.

L’aspetto del contenitore delle miniature è controllato dal seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7thumbnailgridview`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Offset verticale del contenitore delle miniature dalla parte superiore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p>Il margine superiore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p>Il margine sinistro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine destro </span> </p> </td> 
   <td colname="col2"> <p>Il margine destro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom </span> </p> </td> 
   <td colname="col2"> <p>Il margine inferiore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo dell'area miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare le miniature in modo che abbiano una distanza di 32 pixel dalla parte superiore, 5 margini pixel a sinistra e a destra e 8 margini pixel nella parte inferiore, con `0xDDDDDD` sfondo.

```
.s7ecatalogsearchviewer .s7thumbnailgridview { 
 top: 32px; 
 margin-left: 5px; 
 margin-right: 5px; 
 margin-bottom: 8px; 
 background-color: rgb(221, 221, 221); 
}
```

La spaziatura tra le miniature è controllata dal seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumbcell`

<table id="table_1D93AB60E57F49A8838EA825CD6B7897"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p> Dimensione del margine orizzontale e verticale intorno a ciascuna miniatura. La spaziatura effettiva delle miniature orizzontale è uguale alla somma del margine sinistro e destro impostato per <span class="codeph"> .s7thumbcell </span>. La spaziatura verticale delle miniature è uguale alla somma dei margini superiore e inferiore. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare uno spazio di 10 pixel sia verticalmente che orizzontalmente.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumbcell { 
 margin: 5px; 
}
```

L’aspetto di una singola miniatura viene controllato con il seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumb`

<table id="table_1D973EA6C36947F092AAA16CFE9B44A1"> 
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
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sui dispositivi touch, quando viene ruotato in modalità verticale, lo spettatore può ridimensionare le miniature alla metà di quanto configurato nel caso decida di dividere la visualizzazione del catalogo in singole pagine.

>[!NOTE]
>
>La miniatura supporta `state` selettore di attributi, che può essere utilizzato per applicare skin diversi a stati di miniature diversi. In particolare: `state="selected"` corrisponde alla miniatura dell&#39;immagine attualmente visualizzata nella visualizzazione principale, `state="default"` corrisponde al resto delle miniature, e `state="over"` al passaggio del mouse.

Esempio: per impostare miniature di 120 x 85 pixel con sfondo bianco, bordo standard grigio chiaro e bordo selezionato grigio scuro.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumb { 
 width:120px; 
 height:85px; 
 background-color: rgb(255, 255, 255); 
 border: solid 1px #999999; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7thumb[state="selected"]{ 
 border: solid 2px #666666; 
}
```

L’aspetto dell’etichetta delle miniature è controllato dal seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7label`

<table id="table_E242176042F247F8B51A0D5ADB645E20"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nome font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare le etichette in modo che utilizzino il font Helvetica® a 14 pixel.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 12px; 
}
```

Se sono presenti più miniature di quelle che possono rientrare verticalmente nella visualizzazione, la barra di scorrimento verticale viene visualizzata sul lato destro. L’aspetto dell’area della barra di scorrimento è controllato dal seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar`

<table id="table_F05EC87CD9A946DB9B4B2B48E0784168"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> La barra di scorrimento verticale si sposta dalla parte superiore dell'area delle miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>La barra di scorrimento verticale si sposta dalla parte inferiore dell'area delle miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> destra </span> </p> </td> 
   <td colname="col2"> <p> La barra di scorrimento orizzontale si sposta dal bordo destro dell'area delle miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una barra di scorrimento larga 28 pixel con un margine di 8 pixel dalla parte superiore, destra e inferiore dell&#39;area delle miniature.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar { 
 top:8px; 
 bottom:8px; 
 right:8px; 
 width:28px; 
}
```

La traccia della barra di scorrimento è l&#39;area compresa tra i pulsanti di scorrimento superiore e inferiore. Il componente imposta automaticamente la posizione e l&#39;altezza della traccia. Il brano è controllato con il seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack`

<table id="table_EF1B91F9E984451EB0AB48175D917726"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del brano della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del brano della barra di scorrimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una traccia della barra di scorrimento larga 28 pixel e con uno sfondo grigio semitrasparente.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

Il pollice della barra di scorrimento si sposta verticalmente all&#39;interno dell&#39;area della traccia di scorrimento. La sua posizione verticale è completamente controllata dalla logica del componente, tuttavia l’altezza del pollice non cambia in modo dinamico a seconda della quantità di contenuto. L’altezza del pollice e altri aspetti sono controllati con il seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb`

<table id="table_5C791F6E90E64E7A9F1DB7C9B2FDC528"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pollice della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della miniatura della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento superiore </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura verticale tra la parte superiore del brano della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura verticale tra la parte inferiore della traccia della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il miniatura supporta `state` selettore di attributi, che può essere utilizzato per applicare skin diversi agli stati dei pollici `up`, `down`, `over`, e `disabled`.

Esempio: per impostare una barra di scorrimento di 28 x 45 pixel, con margini di 10 pixel in alto e in basso e un disegno diverso per ogni stato.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

L’aspetto dei pulsanti di scorrimento superiore e inferiore è controllato dai seguenti selettori di classi CSS:

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton`

`.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton`

Non è possibile posizionare i pulsanti di scorrimento utilizzando CSS `top`, `left`, `bottom`, e `right` proprietà. Al contrario, la logica di visualizzazione li posiziona automaticamente.

<table id="table_89E64A138ABF463F9650BB454F22D530"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questi pulsanti supportano `state` selettore di attributi, che può essere utilizzato per applicare interfacce diverse ai diversi stati dei pulsanti `up`, `down`, `over`, e `disabled`.

La descrizione comando del pulsante può essere localizzata. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio: per impostare pulsanti di scorrimento di 28 x 32 pixel con grafica diversa per ogni stato.

```
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
