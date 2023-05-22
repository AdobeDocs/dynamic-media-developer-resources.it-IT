---
title: Pannello Risultati ricerca
description: Il pannello dei risultati della ricerca è costituito dalla casella di immissione della ricerca nella parte superiore e dall’area principale in cui vengono visualizzati messaggi informativi o risultati della ricerca.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ffbbc2ae-60da-4c3d-a350-6dbcb64e189d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 1%

---

# Pannello Risultati ricerca{#search-results-panel}

Il pannello dei risultati della ricerca è costituito dalla casella di immissione della ricerca nella parte superiore e dall’area principale in cui vengono visualizzati messaggi informativi o risultati della ricerca.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

Quando il pannello è attivo, l’interfaccia utente del visualizzatore è coperta da un riempimento semitrasparente. Il colore e l&#39;opacità di questo riempimento sono controllati con il seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore della sovrapposizione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità </span> </p> </td> 
   <td colname="col2"> <p>Opacità del colore. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il pannello dei risultati di ricerca occupa sempre tutta l’altezza del visualizzatore disponibile. Tuttavia, è possibile configurare la larghezza. È possibile impostare la larghezza su un valore in pixel assoluto, impostazione predefinita per i punti di interruzione di dimensioni medie e grandi. In alternativa, potete impostare la larghezza su 100% per far sì che il pannello dei risultati di ricerca occupi l&#39;intera area del visualizzatore. La larghezza del pannello è controllata dal seguente selettore di classe CSS:

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

Esempio: per impostare un pannello dei risultati di ricerca di 250 pixel su punti di interruzione di dimensioni medie e grandi e utilizzare un pannello di dimensioni intere su un punto di interruzione di dimensioni ridotte:

```
.s7ecatalogsearchviewer.s7size_large .s7searchpanel .s7searchresultspanel, .s7ecatalogsearchviewer.s7size_medium .s7searchpanel .s7searchresultspanel { 
 width:250px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7searchpanel .s7searchresultspanel { 
 width:100%; 
}
```

La parte superiore del pannello dei risultati di ricerca è dedicata alla casella di input della ricerca. La spaziatura ai lati della casella di input è controllata dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinputcontainer
```

**Proprietà CSS del contenitore di input per la ricerca**

<table id="table_A1B96108542742DC8DCBCC9064F9E90B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura attorno alla casella di input. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il campo di input della ricerca è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput
```

**Proprietà CSS del campo di input della ricerca**

<table id="table_9FB5E89847BF4C889DC22AD7E842C0F7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del campo di input della ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura interna tra i limiti del campo di input e il testo di input. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Bordo del campo di input della ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p>Margine del campo di input della ricerca </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del carattere del testo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un campo di input di ricerca con un’altezza di 0 pixel e un font di testo di 14 pixel:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinput { 
 padding-left:5px; 
 height:30px; 
 font-size:14px; 
}
```

Per impostazione predefinita, il pulsante di ricerca a sinistra del campo di input della ricerca sotto forma di &quot;vetro trasparente&quot; è controllato dal seguente selettore di classe CSS:

```
 .s7ecatalogsearchviewer .s7searchpanel .s7searchinputbutton
```

**Proprietà CSS del pulsante Cerca input**

<table id="table_CDD818B40BB1416CB47B7C52F799DE0C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del pulsante di input per la ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante di input per la ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>L’URL dell’immagine dell’icona "specchio". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione dell'icona "specchio". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Bordo del pulsante di input della ricerca. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p>Margine del pulsante di input per la ricerca. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un pulsante di ricerca con un&#39;icona &quot;vetro&quot; di 26 x 26 pixel; dimensioni di 30 pixel con un bordo di 1 pixel:

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

Il pannello dei risultati della ricerca potrebbe visualizzare un prompt testuale al momento della prima chiamata della funzione. Inoltre, mostra un messaggio quando la ricerca di un utente non ha restituito alcun risultato. In tutti i casi, il testo viene visualizzato nella parte principale del pannello dei risultati di ricerca ed è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nome del carattere del testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>Allineamento orizzontale del testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del testo del carattere. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pannello di testo supporta `state` selettore di attributi, che può essere utilizzato per applicare stili diversi a messaggi di testo diversi. In particolare: `state='prompt'` corrisponde al prompt di testo visualizzato quando si chiama il pannello per la prima volta. Il `state='results'` corrisponde al testo con informazioni sugli hit di ricerca. E infine, `state='no_results'` corrisponde al testo visualizzato quando la query di ricerca non ha restituito alcun risultato.

Il testo del messaggio può essere localizzato. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio: per impostare un pannello di testo che utilizza un font grigio da 18 pixel:

```
.s7ecatalogsearchviewer .s7searchpanel .s7searchinfo { 
 font-size: 18px; 
 color: #696969; 
}
```

I risultati della ricerca vengono visualizzati come una singola colonna o riga di miniature per le pagine con risultati di ricerca. La spaziatura tra le miniature dei risultati di ricerca è controllata con il seguente selettore di classe CSS:

```
.ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell
```

**Proprietà CSS delle celle delle miniature**

<table id="table_26974E509F6943BB98CBC1E4BAE62D68"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine </span> </p> </td> 
   <td colname="col2"> <p> Dimensione del margine verticale intorno a ciascuna miniatura. La spaziatura effettiva delle miniature è uguale alla somma dei margini superiore e inferiore impostati per <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio - Per impostare una spaziatura di dieci pixel:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

L’aspetto delle singole miniature è controllato dal seguente selettore di classe CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb
```

**Proprietà CSS della miniatura**

<table id="table_00829E44F75040A4B2AE19ACD550DA1E"> 
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

Esempio: per impostare miniature di 215 x 129 pixel, con un bordo predefinito grigio chiaro e un bordo selezionato grigio scuro:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7thumb { 
 width: 215px; 
 height: 129px; 
}
```

L’aspetto dell’etichetta delle miniature è controllato dal seguente selettore di classe CSS:

```
 .s7ecatalogsearchviewer 
.s7searchpanel .s7swatches .s7label
```

**Proprietà CSS dell’etichetta**

<table id="table_CA669F6AE7574FF389BF725B3F768E5E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Colore testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nome del carattere del testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del carattere del testo. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare etichette che utilizzano un carattere Helvetica® di 12 pixel, grigio:

```
.s7ecatalogsearchviewer .s7searchpanel .s7swatches .s7label { 
 font-family: Helvetica,sans-serif; 
 color: #4c4c4c; 
 font-size: 12px; 
}
```

Nei sistemi che utilizzano l&#39;input del mouse, nella parte inferiore del pannello dei risultati di ricerca vengono visualizzati due pulsanti di scorrimento che consentono all&#39;utente di scorrere i risultati della ricerca. L’aspetto dei pulsanti di scorrimento verso l’alto o verso il basso è controllato dai seguenti selettori di classi CSS:

```
.s7ecatalogsearchviewer .s7searchpanel .s7scrollupbutton 
.s7ecatalogsearchviewer .s7searchpanel .s7scrolldownbutton
```

Non è possibile posizionare i pulsanti di scorrimento utilizzando le proprietà CSS top, left, bottom e right. Al contrario, la logica di visualizzazione li posiziona automaticamente.

**Proprietà CSS dei pulsanti scorrimento verso l&#39;alto e verso il basso**

<table id="table_11063C7F428D4707A8138F17650F8F5F"> 
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
   <td colname="col2"> <p> Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Posizionate all'interno dello sprite del disegno, se vengono utilizzati gli sprite CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Spunti CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta `state` selettore di attributi, che può essere utilizzato per applicare skin diversi a `"up"`, `"down"`, `"over"`, e `"disabled"` stati dei pulsanti.

Le descrizioni dei pulsanti possono essere localizzate. Consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) per ulteriori informazioni.

Esempio - Per impostare un pulsante di scorrimento verso l&#39;alto di 125 x 35 pixel con immagini diverse per ogni stato:

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
