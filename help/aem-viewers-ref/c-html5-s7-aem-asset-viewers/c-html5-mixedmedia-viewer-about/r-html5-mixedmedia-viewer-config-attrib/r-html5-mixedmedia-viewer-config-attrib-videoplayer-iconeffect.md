---
description: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
uuid: 8e112f3c-8fa6-4c77-94c5-5027275225e7
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 4%

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1 `*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
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

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
