---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---


# FlyoutZoomView.tip{#flyoutzoomview-tip}

` [FlyoutZoomView.|<containerId>_flyout.]tip= *``*[, *``*][, *`durevolationcountfade`*]`

<table id="table_3BA079B51B644219BB8E2A68A13A8D90"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durata</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica il numero di secondi in cui il testo della descrizione viene visualizzato prima che venga nascosto. Se è impostato su <span class="codeph"> -1</span>, il messaggio viene sempre visualizzato, anche se l’utente attiva il riquadro a comparsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica il numero di volte in cui il testo viene visualizzato quando si visualizzano nuove immagini nel set. Il valore <span class="codeph"> -1</span> indica che il testo viene sempre visualizzato quando si visualizza un'immagine nel set. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dissolvenza</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata di un'animazione di dissolvenza che si verifica quando il testo viene visualizzato o scompare. Un valore di <span class="codeph"> 0</span> indica nessuna transizione di dissolvenza. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facoltativo.

## Predefinito {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,1,0.3`

## Esempio {#section-3a188ab955c445bcb2efa3c49722c10d}

`tip=1,-1,0`
