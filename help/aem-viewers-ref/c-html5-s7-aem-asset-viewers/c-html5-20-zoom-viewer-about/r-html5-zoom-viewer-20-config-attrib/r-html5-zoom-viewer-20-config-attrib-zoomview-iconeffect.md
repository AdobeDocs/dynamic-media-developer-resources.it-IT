---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 59d71d3b-706f-4f77-8e75-e24c5654f6e3
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`count`*][, *`dissolvenza`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Abilita <span class="codeph"> iconeffect</span> per essere visualizzata nella parte superiore dell'immagine quando questa è in stato di ripristino e suggerisce un'azione disponibile per interagire con l'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte <span class="codeph"> iconeffect</span> viene visualizzato e ricompare. Un valore di <span class="codeph"> -1</span> indica che l’icona viene sempre visualizzata di nuovo a tempo indefinito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dissolvenza</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata dell'animazione mostra/nascondi, in secondi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Imposta il numero di secondi in cui <span class="codeph"> iconeffect</span> rimane completamente visibile prima che venga nascosto automaticamente. Ossia, il tempo dopo il completamento dell'animazione di dissolvenza in entrata, ma prima dell'inizio dell'animazione di dissolvenza in uscita. Impostazione di <span class="codeph"> 0</span> disabilita il comportamento Nascondi automatico. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1,1,0.3,3`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
