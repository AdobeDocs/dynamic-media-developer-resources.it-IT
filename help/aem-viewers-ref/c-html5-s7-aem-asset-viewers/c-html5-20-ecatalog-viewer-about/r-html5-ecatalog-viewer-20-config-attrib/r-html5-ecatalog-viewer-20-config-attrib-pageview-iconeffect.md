---
description: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: cdd96e58-d805-47d6-bf26-9ebd90afd535
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---

# PageView.iconEffect{#pageview-iconeffect}

` [PageView.|<containerId>_pageView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Abilita l’ <span class="codeph"> iconeffect</span> a essere visualizzato nella parte superiore dell’immagine quando l’immagine è in uno stato di ripristino ed è indicativo di un’azione disponibile per interagire con l’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte in cui l' <span class="codeph"> iconeffect</span> viene visualizzato e rivisualizzato. Un valore di <span class="codeph"> -1</span> indica che l'icona viene sempre visualizzata di nuovo indefinitamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dissolvenza</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata in secondi dell'animazione mostrata o nascosta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Imposta il numero di secondi in cui l' <span class="codeph"> iconeffect</span> rimane completamente visibile prima che si nasconda automaticamente. Cioè, il tempo dopo il completamento dell'animazione di dissolvenza in entrata ma prima dell'avvio dell'animazione di dissolvenza in uscita. Un'impostazione di <span class="codeph"> 0</span> disattiva il comportamento di nascondere automaticamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-b6e5e52698d4492f9d6350e7e312bb1b}

Facoltativo.

## Predefinito {#section-7d0fc8fa09b34c288ed32ef7faa84604}

`1,1,0.3,3`

## Esempio {#section-95db1bfcccf241089654363203b19977}

`iconeffect=0`
