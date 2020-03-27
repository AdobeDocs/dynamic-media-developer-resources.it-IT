---
description: L’indicatore set è una serie di punti sottoposti a rendering nella parte inferiore del visualizzatore. Mostra la posizione corrente all'interno del set.
seo-description: L’indicatore set è una serie di punti sottoposti a rendering nella parte inferiore del visualizzatore. Mostra la posizione corrente all'interno del set.
seo-title: Imposta indicatore
solution: Experience Manager
title: Imposta indicatore
topic: Dynamic media
uuid: 3f90a216-654f-44a9-947d-592bd5f342d4
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Imposta indicatore{#set-indicator}

L’indicatore set è una serie di punti sottoposti a rendering nella parte inferiore del visualizzatore. Mostra la posizione corrente all&#39;interno del set.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;indicatore del set**

L&#39;aspetto del contenitore degli indicatori di set è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo in formato esadecimale dell'indicatore del set. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>L&#39;indicatore set supporta il selettore di attributi mode, che può essere utilizzato per applicare stili diversi per le modalità di funzionamento punteggiate e numeriche. In particolare, `mode="numeric"` corrisponde alla modalità operativa numerica; corrisponde `mode="dotted"` allo stato predefinito del punto.

Esempio: per impostare un indicatore con uno sfondo bianco:

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

L&#39;aspetto di un singolo punto indicatore del set è controllato dal selettore di classe CSS. Si applica agli elementi sia in modalità di operazione punteggiata che numerica.

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
   <td colname="col2"> <p>Larghezza del punto dell’indicatore del set. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del punto dell'indicatore del set. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p>Margine sinistro in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p>Margine superiore in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>Margine destro in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-bottom </span> </p> </td> 
   <td colname="col2"> <p>Margine inferiore in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Raggio del bordo in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo in formato esadecimale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Nome del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Dimensione del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Colore del font. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>Allineamento verticale dell'indice del banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Altezza del testo per l'indice del banner. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Gli indicatori di set supportano il selettore `state` di attributi, che può essere utilizzato per applicare interfacce diverse a stati di miniature diversi. In particolare, `state="selected"` corrisponde all&#39;elemento corrente dell&#39;insieme; corrisponde `state="unselected"` allo stato predefinito dell&#39;elemento.

Esempio: per impostare un indicatore in modalità punteggiata per i sistemi desktop affinché vengano posizionati a 20 pixel dal fondo del visualizzatore. I punti non selezionati sono neri con trasparenza del 50%, 15 x 15 pixel con angoli arrotondati di 7 pixel. I punti selezionati sono neri con trasparenza 90%, 18 x 18 pixel con angoli arrotondati 9 pixel. Lo spazio tra i punti è di 5 pixel.

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

