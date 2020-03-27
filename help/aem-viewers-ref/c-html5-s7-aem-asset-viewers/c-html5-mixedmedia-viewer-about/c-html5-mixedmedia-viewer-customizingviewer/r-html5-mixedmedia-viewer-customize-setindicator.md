---
description: L’indicatore set è una serie di punti rappresentati sopra i campioni principali quando un visualizzatore viene usato su un dispositivo touch. I punti consentono agli utenti di spostarsi tra le pagine delle miniature quando i pulsanti di scorrimento non sono disponibili.
seo-description: L’indicatore set è una serie di punti rappresentati sopra i campioni principali quando un visualizzatore viene usato su un dispositivo touch. I punti consentono agli utenti di spostarsi tra le pagine delle miniature quando i pulsanti di scorrimento non sono disponibili.
seo-title: Imposta indicatore
solution: Experience Manager
title: Imposta indicatore
topic: Dynamic media
uuid: e62fac7c-28b6-40bf-83cc-8bcfbaa0dfa3
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Imposta indicatore{#set-indicator}

L’indicatore set è una serie di punti rappresentati sopra i campioni principali quando un visualizzatore viene usato su un dispositivo touch. I punti consentono agli utenti di spostarsi tra le pagine delle miniature quando i pulsanti di scorrimento non sono disponibili.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**Proprietà CSS dell&#39;indicatore del set**

L&#39;aspetto del contenitore degli indicatori di set è controllato dal seguente selettore di classe CSS:

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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Colore di sfondo in formato esadecimale dell'indicatore del set. </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: per impostare un indicatore con uno sfondo bianco:

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

L’aspetto di un singolo punto indicatore del set è controllato dal selettore di classe CSS:

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
 </tbody> 
</table>

>[!NOTE]
>
>Il punto indicatore impostato supporta il selettore `state` di attributi, che può essere utilizzato per applicare interfacce diverse a stati di miniature diversi. In particolare, `state="selected"` corrisponde alla pagina corrente delle miniature, `state="unselected"` corrispondente allo stato predefinito del punto.

Esempio: per impostare l’indicatore punto su 15 x 15 pixel, con due pixel per il margine orizzontale, cinque pixel per il margine superiore, un pixel per il margine inferiore, dodici pixel per il raggio, #D5D3D3 per il colore predefinito e #939393 per il colore attivo:

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

