---
description: Il sommario è un pulsante situato nella barra di controllo principale. Quando attivato, viene visualizzato un pannello a discesa con un elenco di indici ed etichette di pagina.
solution: Experience Manager
title: Sommario
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1069'
ht-degree: 0%

---


# Sommario{#table-of-contents}

Il sommario è un pulsante situato nella barra di controllo principale. Quando attivato, viene visualizzato un pannello a discesa con un elenco di indici ed etichette di pagina.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

In base alla configurazione, l’elenco può contenere tutte le pagine presenti nel catalogo o solo quelle che hanno etichette esplicite definite. Nei sistemi desktop, se l’elenco è più lungo dello spazio disponibile sullo schermo, viene visualizzata una barra di scorrimento a destra.

La posizione e le dimensioni del pulsante del sommario nell’interfaccia utente del visualizzatore vengono controllate con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7tableofcontents
```

**Proprietà CSS del sommario**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine superiore  </span> </p> </td> 
   <td colname="col2"> <p> Offset dalla parte superiore della barra di controllo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine sinistro  </span> </p> </td> 
   <td colname="col2"> <p> La distanza dal pulsante successivo a sinistra o dal lato sinistro della barra di controllo, se si tratta del primo pulsante di una riga. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse a diversi stati del pulsante.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Esempio: impostare un pulsante sommario posizionato a 4 pixel dal basso e a 43 pixel dalla sinistra della barra di controllo principale; le dimensioni sono di 28 x 28 pixel e per ciascuno dei quattro stati del pulsante viene visualizzata un’immagine diversa:

```
.s7ecatalogsearchviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

L’aspetto del pannello a discesa è controllato con il seguente selettore di classe CSS:

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel
```

**Proprietà CSS del pannello a discesa**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo del pannello a discesa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine  </span> </p> </td> 
   <td colname="col2"> <p> Offset interno tra i bordi del pannello e il contenuto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ombra  </span> </p> </td> 
   <td colname="col2"> <p> Ombreggiatura intorno al pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Non è possibile controllare le dimensioni o la posizione del pannello a discesa da CSS; il componente gestisce il layout a livello di programmazione.

Esempio : configura un pannello a discesa con sfondo nero semitrasparente, un margine di 5 pixel intorno al contenuto e un’ombra esterna:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

L’aspetto e l’aspetto dei singoli elementi sono controllati dal seguente selettore di classi CSS:

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item
```

**Proprietà CSS dell’elemento**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nome carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Altezza dell'oggetto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura interna. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La voce dell’elenco a discesa supporta il selettore di attributi `state` , che può essere utilizzato per applicare interfacce diverse agli stati degli elementi selezionati e al passaggio del mouse.

Esempio: imposta un elemento a discesa con un carattere Helvetica da 14 pixel e un&#39;altezza di 19 pixel. Quando è selezionato, un elemento presenta uno sfondo grigio scuro al passaggio del mouse e uno sfondo grigio chiaro:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

Un elemento che mostra l’indice della pagina è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index
```

**Proprietà CSS dell’indice della pagina**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza minima  </span> </p> </td> 
   <td colname="col2"> <p> Larghezza minima dell’elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza massima  </span> </p> </td> 
   <td colname="col2"> <p> Larghezza massima dell’elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine destro  </span> </p> </td> 
   <td colname="col2"> <p> Distanza tra l’indice della pagina e l’etichetta della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>È possibile nascondere completamente l&#39;indice della pagina impostando `display:none` per la classe CSS `s7index`.

Esempio 1: imposta un indice di pagina con una larghezza minima di 40 pixel, una larghezza massima di 70 pixel e un margine di 5 pixel sul lato destro:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

Esempio 2 - Nascondi indice pagina:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

L’etichetta della pagina è controllata con il seguente selettore di classe CSS:

```
 .s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7label
```

**Proprietà CSS dell’etichetta di pagina**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza minima  </span> </p> </td> 
   <td colname="col2"> <p> Larghezza minima dell’elemento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza massima  </span> </p> </td> 
   <td colname="col2"> <p> Larghezza massima dell’elemento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: imposta un indice di pagina con una larghezza minima di 40 pixel e una larghezza massima di 240 pixel:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

Nel caso in cui siano presenti più elementi di quelli che possono essere inseriti verticalmente nel pannello a discesa e il sistema sia un desktop, il componente esegue il rendering di una barra di scorrimento verticale sul lato destro del pannello. L’aspetto dell’area della barra di scorrimento è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar
```

**Proprietà CSS della barra di scorrimento**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p> Larghezza della barra di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Offset della barra di scorrimento verticale dalla parte superiore dell’area del pannello. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> Offset della barra di scorrimento verticale dal fondo dell'area del pannello. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> right  </span> </p> </td> 
   <td colname="col2"> <p> Offset della barra di scorrimento orizzontale dal bordo destro dell'area del pannello. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: imposta una barra di scorrimento larga 28 pixel e priva di un margine per l’area superiore, destra o inferiore del pannello:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

La traccia della barra di scorrimento è l’area compresa tra i pulsanti di scorrimento superiore e inferiore. Il componente imposta automaticamente la posizione e l&#39;altezza del brano. La traccia viene controllata con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**Proprietà CSS della traccia di scorrimento**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del binario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo del brano. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: imposta una traccia della barra di scorrimento larga 28 pixel e con sfondo grigio semitrasparente:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

Il pollice della barra di scorrimento si sposta verticalmente all’interno dell’area della traccia di scorrimento. La sua posizione verticale è controllata dalla logica del componente. Tuttavia, l’altezza della miniatura non cambia dinamicamente a seconda della quantità di contenuto. Puoi configurare l’altezza del pollice e altri aspetti con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**Proprietà CSS della barra di scorrimento**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>L'altezza del pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura superiore  </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura verticale tra la parte superiore della traccia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imbottitura inferiore  </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura verticale tra il fondo della traccia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un dato stato pollice. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La funzione Thumb supporta il selettore di attributi `state`, che può essere utilizzato per applicare skin diversi agli stati del pollice `up`, `down`, `over` e `disabled`.

Esempio: imposta un pollice della barra di scorrimento di 28 x 45 pixel, presenta 10 margini pixel in alto e in basso e presenta immagini diverse per ogni stato:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

L’aspetto dei pulsanti di scorrimento superiore e inferiore è controllato con i seguenti selettori di classe CSS:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

Non è possibile posizionare i pulsanti di scorrimento utilizzando le proprietà CSS `top`, `left`, `bottom` e `right`; invece, la logica del visualizzatore li posiziona automaticamente.

**Proprietà CSS del pulsante di scorrimento verso l’alto e verso il basso**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il pulsante supporta il selettore di attributi `state`, che può essere utilizzato per applicare skin diversi agli stati del pulsante `up`, `down`, `over` e `disabled`.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Esempio: impostare pulsanti di scorrimento con 28 x 32 pixel e immagini diverse per ogni stato:

```
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```

