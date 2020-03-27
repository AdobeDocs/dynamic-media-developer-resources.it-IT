---
description: 'null'
seo-description: 'null'
seo-title: SpinView.iconeffect
solution: Experience Manager
title: SpinView.iconeffect
topic: Dynamic media
uuid: 864fb8dc-34f8-4216-b38c-cc00f7d8d95f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Consente la visualizzazione dell'effetto <span class="codeph"> icononico</span> nella parte superiore dell'immagine quando l'immagine è in stato di reimpostazione ed è consigliabile un'azione disponibile per interagire con l'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte in cui l'effetto <span class="codeph"> iconoattivo</span> viene visualizzato e riappare. Il valore <span class="codeph"> -1</span> indica che l'icona viene sempre visualizzata di nuovo a tempo indeterminato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dissolvenza</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata in secondi dell'animazione di visualizzazione o nascondere. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Imposta il numero di secondi per cui l’ <span class="codeph"> effetto</span> iconoattivo rimane completamente visibile prima che venga nascosto automaticamente. ovvero il tempo dopo il completamento dell'animazione con dissolvenza in entrata, ma prima dell'inizio dell'animazione con dissolvenza in uscita. L’impostazione <span class="codeph"> 0</span> disattiva il comportamento di disattivazione automatica. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`1,1,0.3,3`

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`iconeffect=0`
