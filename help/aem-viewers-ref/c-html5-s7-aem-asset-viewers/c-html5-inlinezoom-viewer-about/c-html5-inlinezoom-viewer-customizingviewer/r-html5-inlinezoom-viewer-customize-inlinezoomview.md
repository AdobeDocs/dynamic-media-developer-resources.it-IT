---
description: La vista principale è costituita dall’immagine statica, dall’immagine ingrandita visualizzata a comparsa sopra l’immagine statica e dal messaggio di suggerimento visualizzato sopra l’immagine statica.
seo-description: La vista principale è costituita dall’immagine statica, dall’immagine ingrandita visualizzata a comparsa sopra l’immagine statica e dal messaggio di suggerimento visualizzato sopra l’immagine statica.
seo-title: Visualizzazione zoom a comparsa
solution: Experience Manager
title: Visualizzazione zoom a comparsa
topic: Dynamic media
uuid: a918c775-a36a-44e8-9ca4-90cb8f5c3a5e
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 1%

---


# Visualizzazione zoom a comparsa{#flyout-zoom-view}

La vista principale è costituita dall’immagine statica, dall’immagine ingrandita visualizzata a comparsa sopra l’immagine statica e dal messaggio di suggerimento visualizzato sopra l’immagine statica.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

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

Il messaggio di suggerimento può essere localizzato. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27).

.

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

