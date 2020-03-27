---
description: La barra di controllo principale è l’area rettangolare dei sistemi desktop e dei tablet che contengono tutti i controlli dell’interfaccia utente (tranne i pulsanti Pagina grande) disponibili per il visualizzatore eCatalog.
seo-description: La barra di controllo principale è l’area rettangolare dei sistemi desktop e dei tablet che contengono tutti i controlli dell’interfaccia utente (tranne i pulsanti Pagina grande) disponibili per il visualizzatore eCatalog.
seo-title: Barra di controllo principale
solution: Experience Manager
title: Barra di controllo principale
topic: Dynamic media
uuid: 0900f678-d7ec-4653-bc8a-21b8da7d5044
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Barra di controllo principale{#main-control-bar}

La barra di controllo principale è l’area rettangolare dei sistemi desktop e dei tablet che contengono tutti i controlli dell’interfaccia utente (tranne i pulsanti Pagina grande) disponibili per il visualizzatore eCatalog.

Sui telefoni cellulari mantiene ancora i pulsanti Miniature, Sommario, Scarica, Stampa, Preferiti, Condivisione social network, Schermo intero e Chiudi. Tuttavia, i pulsanti Prima pagina e Ultima pagina e l’indicatore pagina vengono rimossi dalla barra di controllo principale e aggiunti alla barra di controllo secondaria. Per impostazione predefinita, la barra di controllo principale viene visualizzata nella parte superiore dell’area del visualizzatore sui sistemi desktop e sui telefoni cellulari e spostata nella parte inferiore dell’area del visualizzatore sui tablet. L’intera larghezza del visualizzatore disponibile viene sempre applicata. È possibile modificarne colore, altezza e posizione verticale nel CSS, rispetto al contenitore del visualizzatore.

L&#39;aspetto della barra di controllo principale è controllato dal seguente selettore di classe CSS:

`.s7ecatalogviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Posizione nella parte superiore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom </span> </p> </td> 
   <td colname="col2"> <p>Posizione nella parte inferiore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della barra di controllo principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della barra di controllo principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** : per impostare una barra di controllo principale grigia alta 36 pixel e posizionata nella parte superiore del contenitore del visualizzatore.

```
.s7ecatalogviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

La barra di controllo principale supporta una funzione di scorrimento opzionale. Viene attivata se la larghezza del visualizzatore è troppo piccola e lo spazio disponibile non è sufficiente per adattarsi a tutti i pulsanti preimpostati nella barra di controllo. In questo caso, nella parte destra della barra di controllo viene visualizzato un pulsante freccia a due stati. Toccando o facendo clic su questo pulsante, tutti gli elementi della barra di controllo scorrono a sinistra o a destra, a seconda dello stato del pulsante di scorrimento. L’esempio più tipico è rappresentato dai dispositivi mobili con schermi di piccole dimensioni con orientamento verticale.

La funzione di scorrimento è attivata per la barra di controllo principale ed è disattivata per la barra di controllo secondaria. La funzione viene attivata e disattivata utilizzando il seguente selettore di classe CSS:

`.s7ecatalogviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> position </span> </p> </td> 
   <td colname="col2"> <p>Se impostata su <span class="codeph"> statica, </span> la funzione di scorrimento è disabilitata. </p> <p>Impostate questa proprietà su <span class="codeph"> assoluta </span> per abilitare la funzione di scorrimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il pulsante di scorrimento viene aggiunto a uno speciale elemento contenitore che posiziona correttamente il pulsante e consente di formattare l&#39;area intorno al pulsante in modo diverso rispetto al resto dello sfondo della barra di controllo, nel caso in cui l&#39;altezza del pulsante di scorrimento sia inferiore all&#39;altezza della barra di controllo.

L&#39;aspetto di questo contenitore di pulsanti di scorrimento è controllato dal seguente selettore di classe CSS:

`.s7ecatalogviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>In genere deve essere uguale o maggiore della larghezza del pulsante di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo del contenitore. </p> </td> 
  </tr> 
 </tbody> 
</table>

È possibile ridimensionare e applicare l&#39;interfaccia al pulsante di scorrimento stesso tramite CSS.

L&#39;aspetto di questo pulsante è controllato dal seguente selettore di classe CSS:

`.s7ecatalogviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
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
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Posizionare all'interno dello sprite della grafica, se vengono utilizzati gli spriti CSS. </p> <p>Consultate anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprite </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta i selettori `state` e `selected` attributo, che possono essere utilizzati per applicare interfacce diverse a stati di pulsante differenti. In particolare, `state="selected"` corrisponde allo stato iniziale del pulsante di scorrimento quando è possibile scorrere il contenuto della barra di controllo verso sinistra; corrisponde `state="default"` allo stato in cui si scorre il contenuto completamente verso sinistra e il pulsante di scorrimento suggerisce di riportarlo allo stato iniziale.

La descrizione del pulsante può essere localizzata. Per ulteriori informazioni, consultate [Localizzazione degli elementi](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) dell&#39;interfaccia utente.

**Esempio** : per abilitare la funzione di scorrimento nella barra di controllo principale per i telefoni cellulari, e impostare un pulsante di scorrimento di 64 x 64 pixel che visualizzi un&#39;immagine diversa per ciascuno dei 4 stati di pulsante diversi se selezionato o non selezionato:

```
.s7ecatalogviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```

