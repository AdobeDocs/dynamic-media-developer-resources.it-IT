---
description: La barra di controllo principale è l’area rettangolare dei sistemi desktop e dei tablet che contengono tutti i controlli dell’interfaccia utente (ad eccezione dei pulsanti Pagina grande) disponibili per il visualizzatore di ricerca eCatalog.
solution: Experience Manager
title: Barra di controllo principale
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Ricerca eCatalog
role: Developer,User
exl-id: cee6a4d4-4099-4bc8-9d67-00a1e963a139
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 1%

---

# Barra di controllo principale{#main-control-bar}

La barra di controllo principale è l’area rettangolare dei sistemi desktop e dei tablet che contengono tutti i controlli dell’interfaccia utente (ad eccezione dei pulsanti Pagina grande) disponibili per il visualizzatore di ricerca eCatalog.

Sui telefoni cellulari, mantiene ancora i pulsanti Miniature, Sommario, Scarica, Stampa, Preferiti, Condivisione social, Schermo intero e Chiudi. Tuttavia, i pulsanti Prima pagina e Ultima pagina e l’indicatore pagina vengono rimossi dalla barra di controllo principale e aggiunti alla barra di controllo secondaria. Per impostazione predefinita, la barra di controllo principale viene visualizzata nella parte superiore dell’area del visualizzatore su sistemi desktop e telefoni cellulari e spostata nella parte inferiore dell’area del visualizzatore su tablet. Richiede sempre l’intera larghezza del visualizzatore disponibile. È possibile modificarne il colore, l’altezza e la posizione verticale nel CSS, rispetto al contenitore del visualizzatore.

L’aspetto della barra di controllo principale viene controllato con il seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dalla parte superiore del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Posizione dal fondo del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della barra di controllo principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo della barra di controllo principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Esempio** : per impostare una barra di controllo principale grigia alta 36 pixel e posizionata nella parte superiore del contenitore del visualizzatore.

```
.s7ecatalogsearchviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

La barra di controllo principale supporta una funzione di scorrimento facoltativa. Viene attivato se la larghezza del visualizzatore è troppo piccola e lo spazio disponibile non è sufficiente per adattarsi a tutti i pulsanti preimpostati nella barra di controllo. In questo caso, nella parte destra della barra di controllo viene visualizzato un pulsante a freccia a due stati. Tocca o fai clic su questo pulsante per scorrere tutti gli elementi della barra di controllo verso sinistra o verso destra, a seconda dello stato del pulsante di scorrimento. Questa funzione è utile soprattutto per i dispositivi mobili con piccoli schermi in orientamento verticale.

La funzione di scorrimento è abilitata per la barra di controllo principale ed è disabilitata per la barra di controllo secondaria. La funzione viene attivata e disattivata utilizzando il seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7controlbar .s7innercontrolbarcontainer`

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
   <td colname="col2"> <p>Quando è impostata su <span class="codeph"> statica </span> la funzione di scorrimento è disabilitata. </p> <p>Imposta questa proprietà su <span class="codeph"> assoluto </span> per abilitare la funzione di scorrimento. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il pulsante di scorrimento viene aggiunto a un elemento contenitore speciale che posiziona correttamente il pulsante e consente di impostare un diverso stile per l’area intorno al pulsante rispetto al resto dello sfondo della barra di controllo nel caso in cui l’altezza del pulsante di scorrimento sia inferiore all’altezza della barra di controllo.

L’aspetto di questo contenitore di pulsanti di scorrimento è controllato con il seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7controlbar .s7scrollbuttoncontainer`

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
   <td colname="col2"> <p>Normalmente deve essere uguale o maggiore della larghezza del pulsante di scorrimento stesso. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo del contenitore. </p> </td> 
  </tr> 
 </tbody> 
</table>

Puoi ridimensionare e applicare lo skin al pulsante di scorrimento stesso tramite CSS.

L’aspetto di questo pulsante è controllato con il seguente selettore di classe CSS:

`.s7ecatalogsearchviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
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
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Vedi anche <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta i selettori di attributi `state` e `selected` , che possono essere utilizzati per applicare interfacce diverse a diversi stati dei pulsanti. In particolare, `state="selected"` corrisponde allo stato iniziale del pulsante di scorrimento quando è possibile scorrere il contenuto della barra di controllo a sinistra; `state="default"` corrisponde allo stato in cui il contenuto viene scortato completamente a sinistra e il pulsante di scorrimento suggerisce di riportarlo allo stato iniziale.

La descrizione comando del pulsante può essere localizzata. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

**Esempio** : per abilitare la funzione di scorrimento nella barra di controllo principale per i telefoni cellulari, e impostare un pulsante di scorrimento di 64 x 64 pixel che mostra un’immagine diversa per ciascuno dei 4 stati di pulsante diversi se selezionato o meno:

```
.s7ecatalogsearchviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogsearchviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```
