---
title: Visualizzazione zoom a comparsa
description: La vista principale è costituita dall'immagine statica e dall'immagine ingrandita mostrata nella vista a comparsa. È inoltre costituita dall'area di navigazione evidenziata visualizzata sopra l'immagine statica e dal messaggio di suggerimento visualizzato sopra l'immagine statica.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 0%

---

# Visualizzazione zoom a comparsa{#flyout-zoom-view}

La vista principale è costituita dall&#39;immagine statica e dall&#39;immagine ingrandita mostrata nella vista a comparsa. È inoltre costituita dall&#39;area di navigazione evidenziata visualizzata sopra l&#39;immagine statica e dal messaggio di suggerimento visualizzato sopra l&#39;immagine statica.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Se le dimensioni dell&#39;immagine visualizzata non corrispondono a quelle della visualizzazione zoom a comparsa, il contenuto dell&#39;immagine viene centrato all&#39;interno dell&#39;area di visualizzazione del rettangolo della visualizzazione zoom a comparsa.

**Proprietà CSS della visualizzazione principale**

L’aspetto della vista principale è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo della visualizzazione principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio - per rendere trasparente la visualizzazione principale:

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**Proprietà CSS della visualizzazione a comparsa**

L’aspetto della vista a comparsa è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> ha lasciato </span> </p> </td> 
   <td colname="col2"> <p> Posizione orizzontale della vista a comparsa, relativa all'angolo superiore sinistro della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primi </span> </p> </td> 
   <td colname="col2"> <p> Posizione verticale della vista a comparsa rispetto all'angolo superiore sinistro della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p> Larghezza della visualizzazione a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza della visualizzazione a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Bordo della visualizzazione a comparsa. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare una visualizzazione a comparsa su 600 x 400 pixel, che viene visualizzata con una distanza di 100 pixel a destra della visualizzazione principale 512 x 288 mostrata nell&#39;esempio precedente:

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**Proprietà CSS dell&#39;evidenziazione nella visualizzazione principale**

L’aspetto dell’evidenziazione nella vista principale è controllato dal seguente selettore di classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

Utilizzando gli stili CSS è possibile controllare sfondo, bordo, trasparenza e attributi simili. Tuttavia, la dimensione e la posizione dell’elemento DOM di evidenziazione sono gestite dalla logica del visualizzatore. La possibilità di ignorarla tramite CSS non è supportata.

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore dell'evidenziazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità </span> </p> </td> 
   <td colname="col2"> <p> Evidenzia opacità. </p> <p>Per Internet Explorer 8, utilizzare <span class="codeph"> filter:alpha(opacity-...) ); </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bordo </span> </p> </td> 
   <td colname="col2"> <p>Il bordo viene evidenziato. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare l&#39;evidenziazione verde con una trasparenza del 40% e un bordo rosso di un pixel:

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**Proprietà CSS del cursore**

Quando il parametro `highlightmode` è impostato su `cursor`, le evidenziazioni nella visualizzazione principale vengono sostituite con immagini del cursore a dimensione fissa, controllate tramite il selettore di classe CSS:

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

È possibile controllare l’immagine e le dimensioni di sfondo utilizzando gli stili CSS.

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
   <td colname="col1"> <p> <span class="codeph"> immagine di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Illustrazione del cursore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p>Larghezza cursore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p>Altezza cursore. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il cursore supporta il selettore di attributi `input`, che può essere utilizzato per applicare disegni e dimensioni del cursore diversi per dispositivi diversi. In particolare, `input="mouse"` corrisponde ai sistemi desktop e `input="touch"` ai dispositivi touch.

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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore sovrapposizione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità </span> </p> </td> 
   <td colname="col2"> <p>Opacità sovrapposizione. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Proprietà CSS del messaggio di suggerimento**

L’aspetto del messaggio di suggerimento è controllato dal seguente selettore di classe CSS:

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

È possibile configurare lo stile, le dimensioni, l&#39;aspetto e l&#39;offset verticale del carattere tramite CSS. Tuttavia, l’allineamento orizzontale viene gestito dalla logica del visualizzatore. L&#39;override tramite CSS tramite le proprietà `left` o `right` non è supportato.

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> in basso </span> </p> </td> 
   <td colname="col2"> <p>Offset dalla parte inferiore della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
   <td colname="col2"> <p>Colore testo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p>Nome font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura intorno al testo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di riempimento di sfondo del testo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raggio bordo </span> </p> </td> 
   <td colname="col2"> <p>Raggio bordo sfondo del testo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità </span> </p> </td> 
   <td colname="col2"> <p>Opacità di sfondo del testo del messaggio. </p> <p>Per Internet Explorer 8, utilizzare <span class="codeph"> filter:alpha(opacity-...) ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Il messaggio di suggerimento può essere localizzato. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27).

Esempio: per impostare un messaggio di suggerimento semitrasparente con il carattere bianco Arial® 12 px, una distanza di 50 pixel dalla parte inferiore della visualizzazione principale, una spaziatura interna e un bordo arrotondato:

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
