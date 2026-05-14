---
title: Visualizzazione zoom a comparsa
description: Nella modalità zoom in linea, la visualizzazione principale è costituita dall'immagine statica. È inoltre costituito dall'immagine ingrandita visualizzata nella finestra a comparsa sull'immagine statica e dal messaggio di suggerimento visualizzato sopra l'immagine statica.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 46c91d1f-5809-4270-a06d-5068d20a6341
TQID: 'https://experienceleague.adobe.com/WANW0VSjIIifkoGyYTkowV8I8jmI7kevWK5etgSbEeo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 265
ht-degree: 0%

---

# Visualizzazione zoom a comparsa{#flyout-zoom-view}

Nella modalità zoom in linea, la visualizzazione principale è costituita dall&#39;immagine statica. È inoltre costituito dall&#39;immagine ingrandita visualizzata nella finestra a comparsa sull&#39;immagine statica e dal messaggio di suggerimento visualizzato sopra l&#39;immagine statica.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;area visualizzatore principale**

L’aspetto della vista principale è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> Colore di sfondo della visualizzazione principale. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio - per rendere trasparente la visualizzazione principale:

```
.s7mixedmediaviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

<!--<a id="section_FD07AB77593748F99DC6C42ED20A61EC"></a>-->

L’aspetto del messaggio di suggerimento è controllato dal seguente selettore di classe CSS:

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip
```

È possibile configurare lo stile del carattere, l&#39;aspetto delle dimensioni e l&#39;offset verticale tramite CSS. Tuttavia, l’allineamento orizzontale viene gestito dalla logica del visualizzatore. L&#39;override tramite CSS tramite le proprietà `left` o `right` non è supportato.

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
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore riempimento sfondo messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raggio bordo </span> </p> </td> 
   <td colname="col2"> <p> Raggio del bordo di sfondo del messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> in basso </span> </p> </td> 
   <td colname="col2"> <p> Offset dalla parte inferiore della vista principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore </span> </p> </td> 
   <td colname="col2"> <p>Colore testo suggerimento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> famiglia di caratteri </span> </p> </td> 
   <td colname="col2"> <p>Famiglia di caratteri. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> opacità </span> </p> </td> 
   <td colname="col2"> <p> Opacità sfondo messaggio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> riempimento </span> </p> </td> 
   <td colname="col2"> <p> Spaziatura intorno al testo del messaggio. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il messaggio di suggerimento può essere localizzato. Per ulteriori informazioni, vedere [Localizzazione degli elementi dell&#39;interfaccia utente](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Esempio: per impostare un messaggio di suggerimento semitrasparente con il carattere bianco Arial® 12 px, 50 pixel di offset dalla parte inferiore della vista principale, spaziatura e un bordo arrotondato:

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
