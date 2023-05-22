---
title: SpinView.iconeffect
description: SpinView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: e84336da-7f33-4fa9-b881-93b9db4bae8b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---

# SpinView.iconeffect{#spinview-iconeffect}

` [SpinView.|<containerId>_spinView.]iconeffect=0|1[, *`count`*][, *`dissolvenza`*][, *`autoHide`*]`

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
   <td colname="col2"> <p>Imposta il numero di secondi in cui <span class="codeph"> iconeffect</span> rimane completamente visibile prima che venga nascosto automaticamente. ovvero il tempo trascorso dal completamento dell'animazione di dissolvenza in entrata, ma prima dell'inizio dell'animazione di dissolvenza in uscita. Impostazione di <span class="codeph"> 0</span> disabilita il comportamento Nascondi automatico. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`1,1,0.3,3`

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`iconeffect=0`
