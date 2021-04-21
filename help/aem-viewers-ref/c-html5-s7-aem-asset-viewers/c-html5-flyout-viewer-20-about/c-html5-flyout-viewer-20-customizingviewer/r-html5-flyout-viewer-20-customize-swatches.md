---
description: I campioni sono costituiti da una riga di miniature con pulsanti di scorrimento opzionali a sinistra e a destra.
solution: Experience Manager
title: Campioni
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 2%

---


# Campioni{#swatches}

I campioni sono costituiti da una riga di miniature con pulsanti di scorrimento opzionali a sinistra e a destra.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

I pulsanti di scorrimento sono visibili sul desktop solo se tutte le miniature non possono adattarsi alla larghezza del contenitore. Sui dispositivi mobili, o se le miniature possono adattarsi alla larghezza del contenitore, i pulsanti di scorrimento non vengono visualizzati.

**Proprietà CSS dei campioni**

L’aspetto del contenitore di campioni è controllato con il seguente selettore di classe CSS:

```
.s7flyoutviewer .s7swatches
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
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza dei campioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza dei campioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> L’offset dei campioni verticali rispetto al contenitore del visualizzatore. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare i campioni su 460 x 100 pixel:

```
.s7flyoutviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

**Proprietà CSS della spaziatura dei campioni di miniatura**

La spaziatura tra le miniature dei campioni viene controllata con il selettore di classe CSS:

```
.s7flyoutviewer .s7swatches .s7thumbcell
```

<table id="table_70FAD50E38EB4647B8FAB832F552BBB8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine  </span> </p> </td> 
   <td colname="col2"> <p> Dimensione del margine orizzontale e verticale intorno a ciascuna miniatura. La spaziatura effettiva delle miniature è uguale alla somma del margine sinistro e destro impostato per <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare la spaziatura su 10 pixel sia verticalmente che orizzontalmente:

```
.s7flyoutviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

**Proprietà CSS dei campioni miniatura**

L’aspetto della singola miniatura è controllato con il seguente selettore di classe CSS:

```
.s7flyoutviewer .s7swatches .s7thumb
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p> Larghezza dei campioni delle miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Altezza dei campioni delle miniature. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Il bordo dei campioni delle miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La miniatura supporta il selettore di attributi `state` , utilizzato per applicare skin diversi a stati di miniatura diversi. In particolare, `state="selected"` corrisponde alla miniatura dell&#39;immagine attualmente visualizzata nella vista principale, `state="default"` corrisponde al resto delle miniature e `state="over"` viene utilizzato al passaggio del mouse.

Esempio : per impostare miniature con 56 x 56 pixel, sono disponibili un bordo grigio chiaro predefinito e un bordo grigio scuro selezionato:

```
.s7flyoutviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7flyoutviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7flyoutviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

**Proprietà CSS dei pulsanti di scorrimento a sinistra e a destra**

L’aspetto dei pulsanti di scorrimento a sinistra e a destra è controllato con i seguenti selettori di classe CSS:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton 
.s7flyoutviewer .s7swatches .s7scrollrightbutton
```

Non è possibile posizionare i pulsanti di scorrimento utilizzando le proprietà CSS `top`, `left`, `bottom` e `right`. Al contrario, la logica del visualizzatore li posiziona automaticamente.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p> Larghezza del pulsante di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Altezza del pulsante di scorrimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Immagine visualizzata per un determinato stato del pulsante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> posizione di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Posizione all’interno dello sprite di un’immagine, se vengono utilizzati gli spriti CSS. </p> <p>Consulta <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> Sprite CSS </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questo pulsante supporta il selettore di attributi `state`, utilizzato per applicare interfacce diverse agli stati del pulsante `up`, `down`, `over` e `disabled`.

Le descrizioni dei pulsanti possono essere localizzate. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) .

Esempio: per impostare pulsanti di scorrimento con 56 x 56 pixel e immagini diverse per ogni stato:

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```

