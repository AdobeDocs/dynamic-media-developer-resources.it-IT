---
description: La vista principale è costituita dall’immagine statica, dall’immagine ingrandita mostrata nella visualizzazione a comparsa, dall’area di navigazione evidenziata visualizzata sull’immagine statica e dal messaggio di suggerimento visualizzato sull’immagine statica.
solution: Experience Manager
title: Visualizzazione zoom a comparsa
feature: Dynamic Media Classic,Visualizzatori,SDK/API,A comparsa
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 2%

---

# Visualizzazione zoom a comparsa{#flyout-zoom-view}

La vista principale è costituita dall’immagine statica, dall’immagine ingrandita mostrata nella visualizzazione a comparsa, dall’area di navigazione evidenziata visualizzata sull’immagine statica e dal messaggio di suggerimento visualizzato sull’immagine statica.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se le dimensioni dell’immagine visualizzata non corrispondono alle dimensioni della visualizzazione a comparsa dello zoom, il contenuto dell’immagine viene centrato all’interno dell’area di visualizzazione rettangolare della visualizzazione a comparsa.

**Proprietà CSS della vista principale**

L’aspetto della vista principale è controllato con il seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo della vista principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per rendere trasparente la visualizzazione principale:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**Proprietà CSS della visualizzazione a comparsa**

L’aspetto della visualizzazione a comparsa è controllato con il seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> sinistra  </span> </p> </td> 
   <td colname="col2"> <p> Posizione orizzontale della vista a comparsa rispetto all’angolo superiore sinistro della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p> Posizione verticale della vista a comparsa rispetto all’angolo superiore sinistro della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Larghezza della vista a comparsa. </p> </td> 
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

**Proprietà CSS dell’evidenziazione nella vista principale**

L’aspetto dell’evidenziazione nella vista principale è controllato con il seguente selettore di classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

È possibile controllare lo sfondo, il bordo, la trasparenza e attributi simili utilizzando CSS. Tuttavia, le dimensioni e la posizione dell’elemento DOM evidenziato sono gestite dalla logica del visualizzatore. Non è supportata la possibilità di bypassarla tramite CSS.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p> Colore dell'evidenziazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità  </span> </p> </td> 
   <td colname="col2"> <p> Evidenzia l'opacità. </p> <p>Per Internet Explorer 8, utilizzare <span class="codeph"> filter:alpha(opacity-...) ); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p>Il bordo è evidenziato. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l’evidenziazione verde con trasparenza del 40% e bordo rosso di un pixel:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**Proprietà CSS del cursore**

Quando il parametro `highlightmode` è impostato su `cursor`, l&#39;evidenziazione si trova nella vista principale viene sostituita da un&#39;immagine cursore a dimensione fissa, controllata dal selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Immagine del cursore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza  </span> </p> </td> 
   <td colname="col2"> <p>Larghezza cursore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza  </span> </p> </td> 
   <td colname="col2"> <p>Altezza del cursore. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il cursore supporta il selettore di attributi `input` , che può essere utilizzato per applicare diverse immagini e dimensioni del cursore per diversi dispositivi. In particolare, `input="mouse"` corrisponde ai sistemi desktop e `input="touch"` corrisponde ai dispositivi touch.

**Proprietà CSS della sovrapposizione**

Quando il parametro `overlay` è impostato su `1`, l&#39;area intorno al fotogramma di evidenziazione o all&#39;immagine del cursore viene controllata con il selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore sovrapposto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità  </span> </p> </td> 
   <td colname="col2"> <p>Sovrapponi opacità. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Proprietà CSS del messaggio di suggerimento**

L’aspetto del messaggio di suggerimento è controllato con il seguente selettore di classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

È possibile configurare lo stile del font, l’aspetto delle dimensioni e l’offset verticale tramite CSS. Tuttavia, l’allineamento orizzontale è gestito dalla logica del visualizzatore. Non è supportata l’override di questa impostazione tramite CSS utilizzando le proprietà `left` o `right` .

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
   <td colname="col2"> <p>Offset dal fondo della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nome carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura intorno al testo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore di riempimento di sfondo del testo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raggio bordo  </span> </p> </td> 
   <td colname="col2"> <p>Raggio del bordo di sfondo del testo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità  </span> </p> </td> 
   <td colname="col2"> <p>Opacità di sfondo del testo del messaggio. </p> <p>Per Internet Explorer 8, utilizza <span class="codeph"> filter:alpha(opacity-..) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Il messaggio di suggerimento può essere localizzato. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) .

Esempio: per impostare un messaggio di suggerimento semitrasparente con font Arial 12px bianco, offset di 50 pixel dal fondo della vista principale, della spaziatura e un bordo arrotondato:

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
