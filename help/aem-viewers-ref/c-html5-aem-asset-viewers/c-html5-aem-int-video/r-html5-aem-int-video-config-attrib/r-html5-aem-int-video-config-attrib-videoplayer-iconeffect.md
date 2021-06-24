---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: VideoPlayer.iconeffect
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Developer,Business Practitioner
exl-id: 690dc488-2db0-4166-a308-f1f3438c480a
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '135'
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
