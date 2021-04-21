---
description: Attributo di configurazione per il visualizzatore video.
solution: Experience Manager
title: VideoPlayer.iconeffect
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Attributo di configurazione per il visualizzatore video.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1 `*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> Abilita IconEffect in modo che venga visualizzato sopra al video quando il video viene messo in pausa. Su alcuni dispositivi vengono utilizzati controlli nativi. In questo caso, il modificatore <span class="codeph"> iconeffect</span> viene ignorato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte in cui viene visualizzato e rivisualizzato IconEffect. Un valore di <span class="codeph"> -1</span> indica che l'icona viene visualizzata nuovamente indefinitamente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> dissolvenza</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica la durata in secondi dell'animazione mostrata o nascosta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> Imposta il numero di secondi in cui IconEffect rimane visibile prima che si nasconda automaticamente. Cioè, il tempo dopo il completamento dell'animazione di dissolvenza in entrata e prima dell'avvio dell'animazione di dissolvenza in uscita. Un'impostazione di <span class="codeph"> 0</span> disattiva il comportamento di nascondere automaticamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```

