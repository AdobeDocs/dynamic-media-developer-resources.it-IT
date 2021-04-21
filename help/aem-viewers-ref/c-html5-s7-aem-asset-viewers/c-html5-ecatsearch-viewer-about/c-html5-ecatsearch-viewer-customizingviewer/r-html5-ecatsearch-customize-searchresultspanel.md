---
description: Il pannello dei risultati della ricerca è costituito dalla casella di immissione ricerca nella parte superiore e dall’area principale in cui vengono visualizzati i messaggi informativi o i risultati della ricerca.
solution: Experience Manager
title: Pannello dei risultati di ricerca
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 1%

---


# Pannello risultati ricerca{#search-results-panel}

Il pannello dei risultati della ricerca è costituito dalla casella di immissione ricerca nella parte superiore e dall’area principale in cui vengono visualizzati i messaggi informativi o i risultati della ricerca.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

Quando il pannello è attivo, l’interfaccia utente del visualizzatore viene coperta da un riempimento semitrasparente. Il colore e l&#39;opacità di questo riempimento vengono controllati con il seguente selettore di classe CSS:

```
.s7ecatalogviewer .s7searchpanel .s7backoverlay
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore della sovrapposizione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità  </span> </p> </td> 
   <td colname="col2"> <p>Opacità del colore. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il pannello dei risultati della ricerca occupa sempre l’altezza di tutti i visualizzatori disponibili. Tuttavia, puoi configurare la larghezza. È possibile impostare la larghezza su un valore in pixel assoluto, che è un’impostazione predefinita per punti di interruzione di medie e grandi dimensioni. Oppure, puoi impostare la larghezza su 100% per fare in modo che il pannello dei risultati di ricerca occupi l’intera area del visualizzatore. La larghezza del pannello è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchresultspace
```

**Proprietà CSS dello spazio dei risultati della ricerca**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza dello spazio dei risultati della ricerca. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un pannello dei risultati di ricerca di 250 pixel su punti di interruzione di grandi e medie dimensioni e utilizzare un pannello di dimensioni complete su un punto di interruzione di piccole dimensioni:

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

La parte superiore del pannello dei risultati della ricerca è dedicata alla casella di input della ricerca. La spaziatura ai lati della casella di input è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**Proprietà CSS del contenitore di input di ricerca**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura intorno alla casella di input. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il campo di input della ricerca è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**Proprietà CSS del campo di immissione ricerca**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del campo di input della ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura sinistra  </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna tra i limiti del campo di input e il testo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Bordo del campo di input della ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine  </span> </p> </td> 
   <td colname="col2"> <p>Margine del campo di immissione ricerca </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del font del testo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un campo di input di ricerca con altezza di 0 pixel e font di testo da 14 pixel:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

Il pulsante di ricerca a sinistra del campo di input di ricerca sotto forma di &quot;vetro che si trova&quot; per impostazione predefinita è controllato dal seguente selettore di classe CSS:

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**Proprietà CSS del pulsante di immissione ricerca**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante di immissione ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante di immissione ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>L’URL dell’immagine a icona "vetro". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> dimensione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>La dimensione dell'icona "vetro". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Bordo del pulsante di input di ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine  </span> </p> </td> 
   <td colname="col2"> <p>Margine del pulsante di immissione ricerca. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un pulsante di ricerca con l’icona &quot;vetro&quot; da 26 x 26 pixel; Dimensioni di 30 pixel con bordo di 1 pixel:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton { 
 width:30px; 
 height:30px; 
 background-size:26px 26px; 
 background-image: url(images/v2/Search_form_field.png); 
 font-size:14px; 
 border: 1px solid #696969; 
}
```

Il pannello dei risultati della ricerca può visualizzare un messaggio di testo quando la funzione viene chiamata per la prima volta. Inoltre, mostra all’utente un messaggio quando la ricerca non ha restituito alcun risultato. In tutti i casi, il testo viene visualizzato nella parte principale del pannello dei risultati della ricerca ed è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo
```

**Proprietà CSS delle informazioni di ricerca**

<table id="table_1DF5A12A21584FCC8C25F170078FEFE6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Colore del testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nome del font del testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align  </span> </p> </td> 
   <td colname="col2"> <p>Allineamento orizzontale del testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del testo del font. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pannello di testo supporta il selettore di attributi `state` , che può essere utilizzato per applicare stili diversi a messaggi di testo diversi. In particolare, `state='prompt'` corrisponde al prompt di testo visualizzato quando il pannello viene chiamato per la prima volta; `state='results'` corrisponde al testo con informazioni sugli hit di ricerca; e `state='no_results'` corrisponde al testo visualizzato quando la query di ricerca non ha restituito alcun risultato.

Il testo del messaggio può essere localizzato. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Esempio : per impostare un pannello di testo che utilizza un font grigio da 18 pixel:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

I risultati della ricerca vengono rappresentati come una singola colonna o una singola riga di miniature per le pagine con hit di ricerca. La spaziatura tra le miniature dei risultati della ricerca è controllata dal seguente selettore di classe CSS:

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**Proprietà CSS delle celle miniature**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine  </span> </p> </td> 
   <td colname="col2"> <p> Dimensione del margine verticale intorno a ciascuna miniatura. La spaziatura effettiva delle miniature è uguale alla somma dei margini superiore e inferiore impostati per <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una spaziatura di 10 pixel:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

L’aspetto delle singole miniature è controllato con il seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**Proprietà CSS della miniatura**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Altezza della miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Bordo della miniatura. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio : per impostare miniature da 215 x 129 pixel, sono disponibili un bordo grigio chiaro predefinito e un bordo grigio scuro selezionato:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

L’aspetto dell’etichetta miniatura è controllato con il seguente selettore di classe CSS:

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**Proprietà CSS dell’etichetta**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> Colore testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nome del font del testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del font del testo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare etichette che utilizzano font da 12 pixel, grigio, Helvetica:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

Nei sistemi che utilizzano l’input del mouse, due pulsanti di scorrimento vengono visualizzati nella parte inferiore del pannello dei risultati della ricerca per consentire all’utente di scorrere i risultati della ricerca. L’aspetto dei pulsanti di scorrimento verso l’alto o verso il basso è controllato dai seguenti selettori di classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

Non è possibile posizionare i pulsanti di scorrimento utilizzando le proprietà CSS in alto, a sinistra, in basso e a destra. Al contrario, la logica del visualizzatore li posiziona automaticamente.

**Proprietà CSS dei pulsanti di scorrimento verso l’alto o verso il basso**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante di scorrimento. </p> </td> 
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
>Questo pulsante supporta il selettore di attributi `state`, che può essere utilizzato per applicare interfacce diverse agli stati dei pulsanti `"up"`, `"down"`, `"over"` e `"disabled"`.

Le descrizioni dei pulsanti possono essere localizzate. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Esempio : per impostare un pulsante di scorrimento verso l’alto di 125 x 35 pixel e con immagini diverse per ogni stato:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton { 
 width:125px; 
 height:35px; 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/searchpanel_scroll_down_disabled.png);
```

