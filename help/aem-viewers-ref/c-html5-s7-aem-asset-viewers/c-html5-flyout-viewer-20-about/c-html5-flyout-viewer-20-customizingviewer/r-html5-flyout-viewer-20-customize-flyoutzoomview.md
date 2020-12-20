---
description: La vista principale è costituita dall’immagine statica, dall’immagine ingrandita mostrata nella visualizzazione a comparsa, dall’area di navigazione evidenziata visualizzata sull’immagine statica e dal messaggio di suggerimento visualizzato sopra l’immagine statica.
seo-description: La vista principale è costituita dall’immagine statica, dall’immagine ingrandita mostrata nella visualizzazione a comparsa, dall’area di navigazione evidenziata visualizzata sull’immagine statica e dal messaggio di suggerimento visualizzato sopra l’immagine statica.
seo-title: Visualizzazione zoom a comparsa
solution: Experience Manager
title: Visualizzazione zoom a comparsa
topic: Dynamic media
uuid: 35c60228-3044-442b-a8e2-e13d0bd306a5
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 1%

---


# Visualizzazione zoom a comparsa{#flyout-zoom-view}

La vista principale è costituita dall’immagine statica, dall’immagine ingrandita mostrata nella visualizzazione a comparsa, dall’area di navigazione evidenziata visualizzata sull’immagine statica e dal messaggio di suggerimento visualizzato sopra l’immagine statica.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se le dimensioni dell’immagine visualizzata non corrispondono alle dimensioni della visualizzazione zoom a comparsa, il contenuto dell’immagine viene centrato all’interno dell’area di visualizzazione rettangolare della visualizzazione zoom a comparsa.

**Proprietà CSS della vista principale**

L&#39;aspetto della vista principale è controllato dal seguente selettore di classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo della vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la vista principale:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**Proprietà CSS della visualizzazione a comparsa**

L&#39;aspetto della visualizzazione a comparsa è controllato dal seguente selettore di classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
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
   <td colname="col1"> <p> <span class="codeph"> left  </span> </p> </td> 
   <td colname="col2"> <p> La posizione orizzontale della vista a comparsa, rispetto all’angolo superiore sinistro della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> La posizione verticale della vista a comparsa, rispetto all’angolo superiore sinistro della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza della visualizzazione a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza della visualizzazione a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Bordo della visualizzazione a comparsa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una visualizzazione a comparsa su 600 x 400 pixel, con uno scostamento di 100 pixel a destra della visualizzazione principale 512 x 288 mostrata nell’esempio precedente:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**Proprietà CSS dell&#39;evidenziazione nella vista principale**

L&#39;aspetto dell&#39;evidenziazione nella vista principale è controllato dal seguente selettore di classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

È possibile controllare gli attributi di sfondo, bordo, trasparenza e simili utilizzando CSS. Tuttavia, la dimensione e la posizione dell’elemento DOM evidenziato vengono gestite dalla logica del visualizzatore. La sostituzione tramite CSS non è supportata.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Colore dell’evidenziazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità  </span> </p> </td> 
   <td colname="col2"> <p> Evidenzia opacità. </p> <p>Per Internet Explorer 8, utilizzare <span class="codeph"> filter:alpha(opacity-...) ); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Il bordo viene evidenziato. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l&#39;evidenziazione verde con trasparenza del 40% e bordo rosso di un pixel:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**Proprietà CSS del cursore**

Quando il parametro `highlightmode` è impostato su `cursor`, l&#39;evidenziazione si trova nella vista principale e viene sostituita da un&#39;immagine cursore a dimensione fissa, controllata dal selettore di classe CSS:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

È possibile controllare l&#39;immagine di sfondo e le dimensioni utilizzando CSS.

Le proprietà CSS applicabili includono:

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Grafica cursore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza cursore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Altezza cursore. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il cursore supporta il selettore di attributi `input`, che può essere utilizzato per applicare grafica e dimensioni diverse del cursore per dispositivi diversi. In particolare, `input="mouse"` corrisponde ai sistemi desktop e `input="touch"` corrisponde ai dispositivi touch.

**Proprietà CSS della sovrapposizione**

Quando il parametro `overlay` è impostato su `1`, l&#39;area intorno al fotogramma di evidenziazione o l&#39;immagine del cursore viene controllata con il selettore di classe CSS:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Colore sovrapposizione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità  </span> </p> </td> 
   <td colname="col2"> <p>Opacità sovrapposizione. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Proprietà CSS del messaggio di suggerimento**

L&#39;aspetto del messaggio di suggerimento è controllato dal seguente selettore di classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

È possibile configurare lo stile del font, l&#39;aspetto delle dimensioni e l&#39;offset verticale tramite CSS. Tuttavia, l&#39;allineamento orizzontale è gestito dalla logica del visualizzatore. La sostituzione tramite CSS utilizzando le proprietà `left` o `right` non è supportata.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p>Consente di scostarsi dal fondo della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nome font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura  </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura intorno al testo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Colore di riempimento di sfondo del testo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>Raggio del bordo di sfondo del testo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità  </span> </p> </td> 
   <td colname="col2"> <p>Opacità di sfondo del testo del messaggio. </p> <p>Per Internet Explorer 8, utilizzare <span class="codeph"> filter:alpha(opacity-...) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Il messaggio di suggerimento può essere localizzato. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27).

Esempio: per impostare un messaggio di suggerimento semi-trasparente con font Arial 12px bianco, l’offset di 50 pixel dal fondo della vista principale, la spaziatura e un bordo arrotondato:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```

