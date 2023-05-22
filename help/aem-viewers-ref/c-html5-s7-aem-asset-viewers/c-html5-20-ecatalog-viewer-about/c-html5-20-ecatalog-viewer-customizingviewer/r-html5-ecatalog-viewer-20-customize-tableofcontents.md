---
title: Sommario
description: Il sommario è un pulsante posizionato nella barra di controllo principale. Quando è attivato, viene visualizzato un pannello a discesa con un elenco di indici ed etichette di pagina.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 9b61e269-201d-4083-9c47-0b73d55aa6ed
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '1061'
ht-degree: 0%

---

# Sommario{#table-of-contents}

Il sommario è un pulsante posizionato nella barra di controllo principale. Quando è attivato, viene visualizzato un pannello a discesa con un elenco di indici ed etichette di pagina.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

In base alla configurazione, l’elenco può contenere tutte le pagine presenti nel catalogo o solo quelle per cui sono definite etichette esplicite. Sui sistemi desktop, se l&#39;elenco è più lungo della superficie disponibile sullo schermo, a destra viene visualizzata una barra di scorrimento.

La posizione e le dimensioni del pulsante del sommario nell’interfaccia utente del visualizzatore sono controllate dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7tableofcontents
```

**Proprietà CSS del sommario**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> Offset dalla parte superiore della barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> Distanza dal pulsante successivo a sinistra o dal lato sinistro della barra di controllo, se si tratta del primo pulsante di una riga. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza del pulsante del sommario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Altezza del pulsante del sommario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta `state` selettore di attributi, che può essere utilizzato per applicare interfacce diverse a stati di pulsante diversi.

La descrizione comando del pulsante può essere localizzata. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio: per impostare un pulsante del sommario posizionato a 4 pixel dal basso e a 43 pixel dalla sinistra della barra di controllo principale. Le dimensioni sono di 28 x 28 pixel e viene visualizzata un&#39;immagine diversa per ciascuno dei quattro diversi stati dei pulsanti:

```
.s7ecatalogviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

L’aspetto del pannello a discesa è controllato dal seguente selettore di classe CSS:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel
```

**Proprietà CSS del pannello a discesa**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del pannello a discesa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p> Offset interno tra i bordi del pannello e il contenuto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p> Ombra esterna attorno al pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Non è possibile controllare le dimensioni o la posizione del pannello a discesa dagli stili CSS; il componente ne gestisce il layout a livello di programmazione.

Esempio: imposta un pannello a discesa con uno sfondo nero semitrasparente, un margine di 5 pixel attorno al contenuto e un’ombra esterna:

```
.s7ecatalogviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

L’aspetto del singolo elemento è controllato dal seguente selettore di classe CSS:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7item
```

**Proprietà CSS dell&#39;elemento**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nome font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell'elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L&#39;elemento dell&#39;elenco a discesa supporta `state` selettore di attributi, che può essere utilizzato per applicare skin diversi agli stati al passaggio del mouse e agli elementi selezionati.

Esempio: impostare un elemento a discesa con un carattere Helvetica® di 14 pixel e un&#39;altezza di 19 pixel. Quando un elemento è selezionato, presenta uno sfondo grigio scuro al passaggio del mouse e uno sfondo grigio chiaro:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

Un elemento che mostra l’indice della pagina è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index
```

**Proprietà CSS dell’indice della pagina**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza minima degli elementi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza massima elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-right </span> </p> </td> 
   <td colname="col2"> <p> Distanza tra l'indice e l'etichetta della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>È possibile nascondere completamente l’indice della pagina impostando `display:none` per `s7index` Classe CSS.

Esempio 1: impostare un indice di pagina con una larghezza minima di 40 pixel, una larghezza massima di 70 pixel e un margine di 5 pixel sul lato destro:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

Esempio 2 - nascondere l’indice della pagina:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

L’etichetta della pagina è controllata con il seguente selettore di classe CSS:

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7label
```

**Proprietà CSS dell’etichetta pagina**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza minima degli elementi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza massima elemento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: impostare un indice di pagina con una larghezza minima di 40 pixel e una larghezza massima di 240 pixel:

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

Se il numero di elementi che possono rientrare verticalmente nel pannello a discesa è maggiore e il sistema è un desktop, il componente esegue il rendering di una barra di scorrimento verticale sul lato destro del pannello. L’aspetto dell’area della barra di scorrimento è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar
```

**Proprietà CSS della barra di scorrimento**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Scostamento della barra di scorrimento verticale dalla parte superiore dell'area del pannello. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p> Scostamento della barra di scorrimento verticale dalla parte inferiore dell'area del pannello. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> destra </span> </p> </td> 
   <td colname="col2"> <p> La barra di scorrimento orizzontale si sposta dal bordo destro dell'area del pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: imposta una barra di scorrimento larga 28 pixel e priva di margini per l’area superiore, destra o inferiore del pannello:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

La traccia della barra di scorrimento è l&#39;area compresa tra i pulsanti di scorrimento superiore e inferiore. Il componente imposta automaticamente la posizione e l&#39;altezza della traccia. Il brano è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**Proprietà CSS del brano di scorrimento**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della traccia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo del brano. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: impostare una traccia della barra di scorrimento larga 28 pixel con uno sfondo grigio semitrasparente:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

Il pollice della barra di scorrimento si sposta verticalmente all&#39;interno dell&#39;area della traccia di scorrimento. La sua posizione verticale è controllata dalla logica del componente. Tuttavia, l’altezza del pollice non cambia in modo dinamico a seconda della quantità di contenuto. Puoi configurare l’altezza del pollice e altri aspetti con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**Proprietà CSS della barra di scorrimento**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento superiore </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura verticale tra la parte superiore del brano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura verticale tra la parte inferiore del brano. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il miniatura supporta `state` selettore di attributi, che può essere utilizzato per applicare skin diversi al `up`, `down`, `over`, e `disabled` stati del pollice.

Esempio: impostare una barra di scorrimento di 28 x 45 pixel, con margini di 10 pixel in alto e in basso e un disegno diverso per ogni stato:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

L’aspetto dei pulsanti di scorrimento superiore e inferiore è controllato dai seguenti selettori di classi CSS:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

Non è possibile posizionare i pulsanti di scorrimento utilizzando CSS `top`, `left`, `bottom`, e `right` proprietà; al contrario, la logica di visualizzazione li posiziona automaticamente.

**Proprietà CSS del pulsante di scorrimento verso l’alto e verso il basso**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il pulsante supporta `state` selettore di attributi, che può essere utilizzato per applicare skin diversi al `up`, `down`, `over`, e `disabled` stati dei pulsanti.

La descrizione comando del pulsante può essere localizzata. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio: impostare pulsanti di scorrimento di 28 x 32 pixel con grafica diversa per ogni stato:

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
