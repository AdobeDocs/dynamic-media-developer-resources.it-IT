---
description: Attributo di configurazione per Visualizzatore video interattivo.
seo-description: Attributo di configurazione per Visualizzatore video interattivo.
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
uuid: a403d44d-d5b5-4d09-876e-39146585704f
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 4%

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Attributo di configurazione per Visualizzatore video interattivo.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Abilita la visualizzazione dell'iconaEffetto nella parte superiore del video quando il video è in stato di pausa. Su alcuni dispositivi vengono utilizzati controlli nativi. In questi casi, il modificatore <span class="codeph"> iconeffect</span> viene ignorato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte in cui viene visualizzato e rivisualizzato IconEffect. Un valore di <span class="codeph"> -1</span> indica che l'icona viene visualizzata nuovamente indefinitamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dissolvenza</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica la durata in secondi dell'animazione mostrata o nascosta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Imposta il numero di secondi in cui IconEffect rimane completamente visibile prima che si nasconda automaticamente. Cioè, il tempo dopo il completamento della dissolvenza nell'animazione e prima dell'inizio della dissolvenza in uscita. Impostare su <span class="codeph"> 0</span> per disabilitare il comportamento di nascondere automaticamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
