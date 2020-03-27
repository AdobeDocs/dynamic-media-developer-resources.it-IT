---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.flyouttransizioni
solution: Experience Manager
title: FlyoutZoomView.flyouttransizioni
topic: Dynamic media
uuid: f1a9f2bc-9a13-4980-9241-e835a0aadd2c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.flyouttransizioni{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|dissolvenza </span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto applicato quando la visualizzazione a comparsa viene visualizzata o nascosta. Con <span class="codeph"> none </span>, l'immagine a comparsa appare immediatamente quando viene attivata e pronta; la <span class="codeph"> diapositiva </span> riproduce l'animazione della diapositiva in direzione da sinistra a destra; La <span class="codeph"> dissolvenza </span> applica una transizione alfa all’immagine a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span></span> </p> </td> 
   <td colname="col2"> <p> Numero di secondi necessari al completamento dell'animazione della presentazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showdelay </span></span> </p> </td> 
   <td colname="col2"> <p> Il ritardo in secondi tra l'azione dell'utente che avvia l'animazione della presentazione e l'inizio della stessa animazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> nascondiglio </span></span> </p> </td> 
   <td colname="col2"> <p> Numero di secondi necessari al completamento dell'animazione Nascondi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ritardo </span></span> </p> </td> 
   <td colname="col2"> <p> Il ritardo in secondi tra l'azione dell'utente che avvia l'animazione Nascondi e l'inizio dell'animazione Nascondi stessa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`fade,1,0,1,0`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`flyouttransition=slide,1,1,2,1`
