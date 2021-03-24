---
description: FlyoutZoomView.tip
solution: Experience Manager
title: FlyoutZoomView.tip
feature: Dynamic Media Classic,Visualizzatori,SDK/API,A comparsa
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
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

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,1,0.3`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`tip=1,-1,0`
