---
description: 'null'
seo-description: 'null'
seo-title: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
topic: Dynamic media
uuid: c8d63ad9-6867-4b90-a113-6a75e394f706
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.iconEffect{#pageview-iconeffect}

[!DNL `[PageView.|<containerId>_pageView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`]

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
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

## Proprietà {#section-b6e5e52698d4492f9d6350e7e312bb1b}

Facoltativo.

## Predefinito {#section-7d0fc8fa09b34c288ed32ef7faa84604}

[!DNL `1,1,0.3,3`]

## Esempio {#section-95db1bfcccf241089654363203b19977}

[!DNL `iconeffect=0`]
