---
description: L’indicatore set è una serie di punti sottoposti a rendering sui campioni principali quando un visualizzatore viene utilizzato su un dispositivo touch. I punti consentono agli utenti di spostarsi tra le pagine delle miniature quando i pulsanti di scorrimento non sono disponibili.
solution: Experience Manager
title: Imposta indicatore
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: 53ee058a-cb8c-4b1f-bb9b-caaecc12c947
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# Imposta indicatore{#set-indicator}

L’indicatore set è una serie di punti sottoposti a rendering sui campioni principali quando un visualizzatore viene utilizzato su un dispositivo touch. I punti consentono agli utenti di spostarsi tra le pagine delle miniature quando i pulsanti di scorrimento non sono disponibili.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell’indicatore set**

L’aspetto del contenitore dell’indicatore set è controllato con il seguente selettore di classe CSS:

```
.s7mixedmediaviewer .s7setindicator
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

Esempio: per impostare un indicatore con sfondo bianco:

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

L’aspetto di un singolo punto indicatore del set è controllato con il selettore di classe CSS:

`.s7mixedmediaviewer .s7setindicator .s7dot`

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
 </tbody> 
</table>

>[!NOTE]
>
>Il punto indicatore impostato supporta il selettore di attributi `state`, che può essere utilizzato per applicare skin diversi a stati di miniatura diversi. In particolare, `state="selected"` corrisponde alla pagina corrente delle miniature, `state="unselected"` corrisponde allo stato predefinito del punto.

Esempio: per impostare un punto indicatore a 15 x 15 pixel, con due pixel di margine orizzontale, cinque pixel di margine superiore, un margine inferiore di un pixel, un raggio di dodici pixel, #D5D3D3 colore predefinito e #939393 colore attivo:

```
.s7mixedmediaviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7mixedmediaviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
