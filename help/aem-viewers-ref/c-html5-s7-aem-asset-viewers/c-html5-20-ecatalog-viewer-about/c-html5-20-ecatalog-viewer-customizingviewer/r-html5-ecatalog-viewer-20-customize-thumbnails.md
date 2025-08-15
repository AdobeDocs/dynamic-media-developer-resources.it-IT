---
title: Miniature
description: Le miniature sono costituite da una griglia di miniature con una barra di scorrimento opzionale sul lato destro per consentire lo scorrimento verticale.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3d3d33b-f6bb-4c5b-820c-028bfb6b2594
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# Miniature{#thumbnails}

Le miniature sono costituite da una griglia di miniature con una barra di scorrimento opzionale sul lato destro per consentire lo scorrimento verticale.

Per attivare o disattivare le miniature, fai clic sul pulsante delle miniature nella barra di controllo principale. Quando le miniature sono attive, vengono visualizzate in modalità modale sovrapposte all&#39;interfaccia utente del visualizzatore. La logica visualizzatore ridimensiona automaticamente il contenitore delle miniature nell&#39;intera area visualizzatore.

L&#39;aspetto del contenitore delle miniature è controllato con la seguente classe CSS selettore:

`.s7ecatalogviewer .s7thumbnailgridview`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> In alto </span> </p> </td> 
   <td colname="col2"> <p> Offset verticale del contenitore delle miniature dalla parte superiore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine superiore </span> </p> </td> 
   <td colname="col2"> <p>Margine superiore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Margine sinistro </span> </p> </td> 
   <td colname="col2"> <p>Margine sinistro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Margine destro </span> </p> </td> 
   <td colname="col2"> <p>Il margine destro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine inferiore </span> </p> </td> 
   <td colname="col2"> <p>Il margine inferiore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo dell'area miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare le miniature in modo che abbiano uno scostamento di 32 pixel dall&#39;alto, margini di 5 pixel a sinistra e a destra e margine di 8 pixel in basso, con `0xDDDDDD` sfondo.

```
.s7ecatalogviewer .s7thumbnailgridview { 
 top: 32px; 
 margin-left: 5px; 
 margin-right: 5px; 
 margin-bottom: 8px; 
 background-color: rgb(221, 221, 221); 
}
```

La spaziatura tra le miniature è controllata con la seguente classe CSS selettore:

`.s7ecatalogviewer .s7thumbnailgridview .s7thumbcell`

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
   <td colname="col2"> <p> Dimensione del margine orizzontale e verticale attorno a ciascuna miniatura. La spaziatura orizzontale effettiva delle miniature è uguale alla somma del margine sinistro e destro impostato per <span class="codeph"> .s7thumbcell </span>. La spaziatura verticale delle miniature equivale alla somma del margine superiore e inferiore. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare uno spazio di 10 pixel sia verticalmente che orizzontalmente.

```
.s7ecatalogviewer .s7thumbnailgridview .s7thumbcell { 
 margin: 5px; 
}
```

L&#39;aspetto delle singole miniature è controllato con la seguente classe CSS selettore:

`.s7ecatalogviewer .s7thumbnailgridview .s7thumb`

<table id="table_1D973EA6C36947F092AAA16CFE9B44A1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> confine </span> </p> </td> 
   <td colname="col2"> <p>Il bordo dell'anteprima. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sui dispositivi touch, quando ruota in modalità verticale, il visualizzatore può ridimensionare le miniature alla metà di quanto configurato nel caso in cui decida di suddividere il catalogo distribuito in singole pagine.

>[!NOTE]
>
>La miniatura supporta il `state` selettore attributi, che può essere utilizzato per applicare interfacce diverse a diversi stati di miniatura. In particolare, `state="selected"` corrisponde alla miniatura dell&#39;immagine che viene attualmente visualizzata nella vista principale, `state="default"` corrisponde al resto delle miniature e `state="over"` viene utilizzata al passaggio del mouse.

Esempio: per impostare miniature di 120 x 85 pixel con sfondo bianco, bordo standard grigio chiaro e bordo selezionata in grigio scuro.

```
.s7ecatalogviewer .s7thumbnailgridview .s7thumb { 
 width:120px; 
 height:85px; 
 background-color: rgb(255, 255, 255); 
 border: solid 1px #999999; 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7thumb[state="selected"]{ 
 border: solid 2px #666666; 
}
```

L&#39;aspetto dell&#39;etichetta della miniatura è controllato con i seguenti selettore di classe CSS:

`.s7ecatalogviewer .s7thumbnailgridview .s7label`

<table id="table_E242176042F247F8B51A0D5ADB645E20"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p>Nome font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Dimensioni font </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio - per impostare le etichette per l&#39;utilizzo di 14 pixel Helvetica® font.

```
.s7ecatalogviewer .s7thumbnailgridview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 12px; 
}
```

Se sono presenti più miniature di quelle che possono essere inserite verticalmente nella visualizzazione, le miniature eseguono il rendering della barra di scorrimento verticale sul lato destro. L&#39;aspetto dell&#39;area della barra di scorrimento è controllato con la seguente classe CSS selettore:

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar`

<table id="table_F05EC87CD9A946DB9B4B2B48E0784168"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> In alto </span> </p> </td> 
   <td colname="col2"> <p> Offset della barra di scorrimento verticale rispetto alla parte superiore dell'area delle miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Fondoschiena </span> </p> </td> 
   <td colname="col2"> <p>Offset della barra di scorrimento verticale rispetto alla parte inferiore dell'area delle miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A destra </span> </p> </td> 
   <td colname="col2"> <p> Offset della barra di scorrimento orizzontale dal bordo destro dell'area delle miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una barra di scorrimento larga 28 pixel con un margine di 8 pixel dalla parte superiore, destra e inferiore dell&#39;area delle miniature.

```
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar { 
 top:8px; 
 bottom:8px; 
 right:8px; 
 width:28px; 
}
```

La traccia della barra di scorrimento è l&#39;area compresa tra i pulsanti di scorrimento superiore e inferiore. Il componente imposta automaticamente la posizione e l&#39;altezza della traccia. La traccia è controllata con la seguente classe CSS selettore:

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack`

<table id="table_EF1B91F9E984451EB0AB48175D917726"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della traccia della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del brano della barra di scorrimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una traccia della barra di scorrimento larga 28 pixel e con uno sfondo grigio semitrasparente.

```
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

Il pollice della barra di scorrimento si sposta verticalmente all&#39;interno dell&#39;area della traccia di scorrimento. La sua posizione verticale è completamente controllata dalla logica del componente, tuttavia, l&#39;altezza del pollice non cambia dinamicamente a seconda della quantità di contenuto. L&#39;altezza del pollice e altri aspetti sono controllati con la seguente classe CSS selettore:

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb`

<table id="table_5C791F6E90E64E7A9F1DB7C9B2FDC528"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pollice della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza della miniatura della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento superiore </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura verticale tra la parte superiore della traccia della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura inferiore </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura verticale tra la parte inferiore della traccia della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all'interno dello sprite dell'illustrazione, se vengono utilizzati sprite CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb supporta l&#39;attributo `state` selettore, che può essere utilizzato per applicare interfacce diverse agli stati `up`del pollice , `down`, `over`, e `disabled`.

Esempio: per impostare un pollice della barra di scorrimento di 28 x 45 pixel, con margini di 10 pixel in alto e in basso e con una grafica diversa per ogni stato.

```
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

L&#39;aspetto dei pulsanti di scorrimento superiore e inferiore è controllato con i seguenti selettori di classe CSS:

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton`

`.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton`

Non è possibile posizionare i pulsanti di scorrimento utilizzando CSS `top`, `left`, `bottom`, e `right` proprietà. Al contrario, la logica visualizzatore li posiziona automaticamente.

<table id="table_89E64A138ABF463F9650BB454F22D530"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza della pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione sfondo </span> </p> </td> 
   <td colname="col2"> <p> Posizione all'interno dello sprite dell'illustrazione, se vengono utilizzati sprite CSS. </p> <p>Vedere anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questi pulsanti supportano l&#39;attributo `state` selettore, che può essere utilizzato per applicare interfacce diverse ai diversi stati `up`pulsante , `down`, `over`e `disabled`.

Il suggerimento strumento pulsante può essere localizzato. Per ulteriori informazioni, consulta [Localizzazione di utente elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) dell&#39;interfaccia.

Esempio - per impostare pulsanti di scorrimento che sono 28 x 32 pixel e hanno grafica diversa per ogni stato.

```
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogviewer .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
