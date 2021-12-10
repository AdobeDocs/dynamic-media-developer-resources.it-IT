---
title: Imposta indicatore
description: L’indicatore set è una serie di punti sottoposti a rendering sui campioni quando un visualizzatore viene utilizzato su un dispositivo touch. I punti consentono agli utenti di spostarsi tra le pagine delle miniature quando i pulsanti di scorrimento non sono disponibili.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: b1e6734e-a341-45d7-b771-daeb0527cd00
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---

# Imposta indicatore{#set-indicator}

L’indicatore set è una serie di punti sottoposti a rendering sui campioni quando un visualizzatore viene utilizzato su un dispositivo touch. I punti consentono agli utenti di spostarsi tra le pagine delle miniature quando i pulsanti di scorrimento non sono disponibili.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’indicatore set**

L’aspetto del contenitore dell’indicatore set è controllato con il seguente selettore di classe CSS:

```
.s7zoomviewer .s7setindicator
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
   <td colname="col2"> <p>Colore di sfondo in formato esadecimale dell'indicatore set. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per creare un indicatore impostato con sfondo bianco:

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

L’aspetto di un singolo punto indicatore del set è controllato con il selettore di classe CSS:

`.s7zoomviewer .s7setindicator .s7dot`

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
   <td colname="col1"> <p> <span class="codeph"> margine sinistro </span> </p> </td> 
   <td colname="col2"> <p>Margine sinistro in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine superiore </span> </p> </td> 
   <td colname="col2"> <p>Margine superiore in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine destro </span> </p> </td> 
   <td colname="col2"> <p>Margine destro in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margine inferiore </span> </p> </td> 
   <td colname="col2"> <p>Margine inferiore in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> raggio bordo </span> </p> </td> 
   <td colname="col2"> <p>Raggio del bordo in pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo in formato esadecimale. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Imposta il punto indicatore supporta `state` selettore di attributi, che può essere utilizzato per applicare skin diversi a diversi stati di miniatura. In particolare, `state="selected"` corrisponde alla pagina corrente delle miniature, `state="unselected"` corrisponde allo stato predefinito del punto.

Esempio: per creare un punto indicatore impostato da 15 x 15 pixel, con un margine orizzontale di 2 pixel, un margine superiore di 5 pixel, un margine inferiore di 1 pixel, un raggio di 12 pixel, un colore predefinito #D5D3D3 e un colore attivo #939393:

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
