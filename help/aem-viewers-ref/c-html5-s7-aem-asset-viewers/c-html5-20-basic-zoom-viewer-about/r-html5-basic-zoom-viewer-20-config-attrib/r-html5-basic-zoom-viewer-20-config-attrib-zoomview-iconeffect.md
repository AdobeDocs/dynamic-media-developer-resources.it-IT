---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: faec00b3-b981-4831-bc97-dff442389133
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`count`*][, *`dissolvenza`*][, *`autoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Abilita IconEffect a essere visualizzato nella parte superiore dell'immagine quando l'immagine è in uno stato di ripristino ed è indicativo di un'azione disponibile per interagire con l'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte in cui viene visualizzato e rivisualizzato IconEffect. Un valore di <span class="codeph"> -1</span> indica che l’icona viene sempre visualizzata a tempo indefinito. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dissolvenza</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata in secondi dell'animazione mostrata o nascosta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p>Imposta il numero di secondi in cui IconEffect rimane completamente visibile prima che si nasconda automaticamente. Cioè, il tempo dopo il completamento dell'animazione di dissolvenza in entrata ma prima dell'avvio dell'animazione di dissolvenza in uscita. Impostazione di <span class="codeph"> 0</span> disabilita il comportamento di nascondere automaticamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-50bcd15223174bb79ce08b31ea03d682}

Facoltativo.

## Predefinito {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## Esempio {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`
