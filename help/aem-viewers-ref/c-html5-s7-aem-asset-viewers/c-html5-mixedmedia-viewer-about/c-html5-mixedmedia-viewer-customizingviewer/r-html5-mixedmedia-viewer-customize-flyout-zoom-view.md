---
description: Nella modalità zoom in linea la visualizzazione principale è costituita dall’immagine statica, dall’immagine ingrandita visualizzata nella visualizzazione a comparsa sull’immagine statica e dal messaggio di suggerimento visualizzato sull’immagine statica.
solution: Experience Manager
title: Visualizzazione zoom a comparsa
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: 46c91d1f-5809-4270-a06d-5068d20a6341
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 3%

---

# Visualizzazione zoom a comparsa{#flyout-zoom-view}

Nella modalità zoom in linea la visualizzazione principale è costituita dall’immagine statica, dall’immagine ingrandita visualizzata nella visualizzazione a comparsa sull’immagine statica e dal messaggio di suggerimento visualizzato sull’immagine statica.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’area visualizzatore principale**

L’aspetto della vista principale è controllato con il seguente selettore di classe CSS:

```
.s7mixedmediaviewer .s7flyoutzoomview
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
.s7mixedmediaviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

<!--<a id="section_FD07AB77593748F99DC6C42ED20A61EC"></a>-->

L’aspetto del messaggio di suggerimento è controllato con il seguente selettore di classe CSS:

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip
```

È possibile configurare lo stile del font, l’aspetto delle dimensioni e l’offset verticale tramite CSS. Tuttavia, l’allineamento orizzontale è gestito dalla logica del visualizzatore. Non è supportata l’override di questa impostazione tramite CSS utilizzando le proprietà `left` o `right` .

**Proprietà CSS del messaggio di suggerimento**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore di riempimento dello sfondo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raggio bordo  </span> </p> </td> 
   <td colname="col2"> <p> Raggio del bordo dello sfondo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bottom  </span> </p> </td> 
   <td colname="col2"> <p> Offset dal fondo della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore testo punta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del carattere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di caratteri. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità  </span> </p> </td> 
   <td colname="col2"> <p> Opacità di sfondo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> spaziatura interna  </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura intorno al testo del messaggio. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il messaggio di suggerimento può essere localizzato. Per ulteriori informazioni, consulta [Localizzazione degli elementi dell’interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) .

Esempio: per impostare un messaggio di suggerimento semitrasparente con font Arial 12px bianco, l’offset di 50 pixel dal fondo della vista principale, della spaziatura e di un bordo arrotondato:

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip { 
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
