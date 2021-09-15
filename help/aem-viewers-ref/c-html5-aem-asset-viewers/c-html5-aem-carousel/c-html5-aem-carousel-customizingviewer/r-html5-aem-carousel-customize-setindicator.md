---
title: Imposta indicatore
description: L'indicatore set è una serie di punti sottoposti a rendering nella parte inferiore del visualizzatore. Mostra la posizione corrente all’interno del set.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 1%

---

# Imposta indicatore{#set-indicator}

L&#39;indicatore set è una serie di punti sottoposti a rendering nella parte inferiore del visualizzatore. Mostra la posizione corrente all’interno del set.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’indicatore set**

L’aspetto del contenitore dell’indicatore set è controllato con il seguente selettore di classe CSS:

```
.s7carouselviewer .s7setindicator
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
   <td colname="col2"> <p>Colore di sfondo in formato esadecimale dell'indicatore set. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L&#39;indicatore set supporta il selettore di attributi della modalità, che può essere utilizzato per applicare stili diversi per le modalità di funzionamento punteggiate e numeriche. In particolare, `mode="numeric"` corrisponde alla modalità operativa numerica; `mode="dotted"` corrisponde allo stato predefinito del punto.

Ad esempio, supponi di voler impostare un indicatore di set con sfondo bianco:

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

L’aspetto di un singolo punto indicatore del set è controllato con il selettore di classe CSS. Si applica agli elementi sia in modalità di funzionamento punteggiata che numerica.

`.s7carouselviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Proprietà CSS </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Larghezza del punto dell'indicatore impostato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del punto indicatore impostato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine sinistro  </span> </p> </td> 
   <td colname="col2"> <p>Margine sinistro in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine superiore  </span> </p> </td> 
   <td colname="col2"> <p>Margine superiore in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine destro  </span> </p> </td> 
   <td colname="col2"> <p>Margine destro in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine inferiore  </span> </p> </td> 
   <td colname="col2"> <p>Margine inferiore in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raggio bordo  </span> </p> </td> 
   <td colname="col2"> <p>Raggio del bordo in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo  </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo in formato esadecimale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Nome del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> allineamento verticale  </span> </p> </td> 
   <td colname="col2"> <p>Allineamento verticale dell'indice del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza riga  </span> </p> </td> 
   <td colname="col2"> <p>Altezza del testo per l'indice del banner. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Gli elementi degli indicatori impostati supportano il selettore di attributi `state` , che può essere utilizzato per applicare skin diversi a diversi stati di miniatura. In particolare, `state="selected"` corrisponde all’elemento corrente nel set; `state="unselected"` corrisponde allo stato predefinito dell&#39;elemento.

Ad esempio, si supponga di voler impostare un indicatore di set in modalità punteggiata per i sistemi desktop. Desideri che sia posizionato a 20 pixel dal fondo del visualizzatore. Inoltre, vuoi che i punti non selezionati siano neri con una trasparenza del 50%, 15 x 15 pixel con sette angoli arrotondati. I punti selezionati sono neri con trasparenza del 90%, 18 x 18 pixel con angoli arrotondati di nove pixel. Lo spazio tra i punti è di cinque pixel.

```
.s7carouselviewer.s7mouseinput .s7setindicator { 
 bottom: 20px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot{ 
 width:15px; 
 height:15px; 
 margin-left:2.5px; 
 margin-right:2.5px; 
 margin-top:2.5px; 
 margin-bottom:2.5px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='selected'] {  
 width:18px; 
 height:18px; 
 background-color: #000000; 
 opacity: 0.9; 
 border-radius:9px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='unselected'] {  
 width:15px; 
 height:15px; 
 background-color: #000000; 
 opacity: 0.5; 
 border-radius:7px; 
}
```
