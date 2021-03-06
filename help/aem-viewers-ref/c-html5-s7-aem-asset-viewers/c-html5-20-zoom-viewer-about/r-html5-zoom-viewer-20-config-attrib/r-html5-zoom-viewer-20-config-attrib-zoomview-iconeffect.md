---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 59d71d3b-706f-4f77-8e75-e24c5654f6e3
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`count`*][, *`dissolvenza`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Abilita la <span class="codeph"> iconEffetto</span> per visualizzare nella parte superiore dell'immagine quando l'immagine è in stato di reset ed è indicativo di un'azione disponibile per interagire con l'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte in cui il <span class="codeph"> iconEffetto</span> appare e riappare. Un valore di <span class="codeph"> -1</span> indica che l’icona viene sempre visualizzata a tempo indefinito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dissolvenza</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata in secondi dell'animazione mostrata o nascosta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Imposta il numero di secondi in cui la <span class="codeph"> iconEffetto</span> rimane completamente visibile prima che si nasconda automaticamente. Cioè, il tempo dopo il completamento dell'animazione di dissolvenza in entrata ma prima dell'avvio dell'animazione di dissolvenza in uscita. Impostazione di <span class="codeph"> 0</span> disabilita il comportamento di nascondere automaticamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1,1,0.3,3`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
