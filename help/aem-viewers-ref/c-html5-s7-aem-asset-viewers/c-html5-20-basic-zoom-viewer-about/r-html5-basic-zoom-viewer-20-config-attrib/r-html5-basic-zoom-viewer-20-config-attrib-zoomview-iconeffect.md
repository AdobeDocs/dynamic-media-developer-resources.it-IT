---
description: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
topic: Dynamic media
uuid: 38350e3d-515b-454c-bc85-39b91ad06e8b
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---


# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Abilita IconEffect a visualizzare nella parte superiore dell'immagine quando l'immagine è in stato di ripristino ed è consigliabile un'azione disponibile per interagire con l'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte in cui IconEffect viene visualizzato e riappare. Un valore di <span class="codeph"> -1</span> indica che l'icona viene sempre visualizzata a tempo indeterminato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dissolvenza</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata in secondi dell'animazione di visualizzazione o nascondere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p>Imposta il numero di secondi per cui IconEffect rimane completamente visibile prima che venga nascosto automaticamente. ovvero il tempo dopo il completamento dell'animazione con dissolvenza in entrata, ma prima dell'inizio dell'animazione con dissolvenza in uscita. Un'impostazione di <span class="codeph"> 0</span> disattiva il comportamento di disattivazione automatica. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-50bcd15223174bb79ce08b31ea03d682}

Facoltativo.

## Predefinito {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## Esempio {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`
