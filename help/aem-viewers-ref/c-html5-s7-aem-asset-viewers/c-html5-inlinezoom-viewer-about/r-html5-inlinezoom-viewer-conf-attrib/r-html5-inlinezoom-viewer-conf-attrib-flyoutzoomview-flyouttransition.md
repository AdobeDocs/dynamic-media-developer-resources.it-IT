---
description: FlyoutZoomView.flyouttransition
solution: Experience Manager
title: FlyoutZoomView.flyouttransition
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---


# FlyoutZoomView.flyouttransition{#flyoutzoomview-flyouttransition}

` [FlyoutZoomView.|<containerId>_flyout.]flyouttransition=[none|slide|fade][, *``*[, *``*[, *``*[, *`showtimeshowdelayhidetimehidedelay`*]]]]`

<table id="table_AB421835D2454ECD8AA40DBFADBAC65F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|slide|dissolvenza  </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica il tipo di effetto applicato quando la visualizzazione a comparsa viene visualizzata o nascosta. Con <span class="codeph"> nessuno </span>, l'immagine a comparsa viene visualizzata istantaneamente quando attivata e pronta; <span class="codeph"> diapositiva </span> riproduce l'animazione della diapositiva in direzione da sinistra a destra; <span class="codeph"> dissolvenza </span> applica una transizione alfa all'immagine a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spettacolo  </span> </span> </p> </td> 
   <td colname="col2"> <p> Numero di secondi necessari al completamento dell'animazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> vetrina  </span> </span> </p> </td> 
   <td colname="col2"> <p> Il ritardo in secondi tra l'azione dell'utente che avvia l'animazione della mostra e l'inizio dell'animazione della mostra stessa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> tempo cupo  </span> </span> </p> </td> 
   <td colname="col2"> <p> Numero di secondi necessari al completamento dell'animazione di nascondi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ritardo  </span> </span> </p> </td> 
   <td colname="col2"> <p> Il ritardo in secondi tra l'azione dell'utente che avvia l'animazione di default e l'inizio di nascondere l'animazione stessa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

`fade,1,0,1,0`

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`flyouttransition=slide,1,1,2,1`
