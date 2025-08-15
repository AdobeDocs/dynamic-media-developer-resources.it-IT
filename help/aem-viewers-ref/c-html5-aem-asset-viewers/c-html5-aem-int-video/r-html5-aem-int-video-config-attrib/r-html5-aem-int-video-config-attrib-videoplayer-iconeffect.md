---
title: VideoPlayer.iconeffect
description: Attributo di configurazione per visualizzatore Video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 690dc488-2db0-4166-a308-f1f3438c480a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 2%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

Attributo di configurazione per visualizzatore Video interattivo.

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *``*][, *`Nascondi automaticamente dissolvenza conteggio`*][, *``*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Consente di visualizzare IconEffect sopra il video quando il video si trova in pausa. In alcuni dispositivi vengono utilizzati controlli nativo. In tal caso, il <span class="codeph"> modificatore iconeffect</span> viene ignorato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> contare</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il numero massimo di volte in cui IconEffect appare e riappare. Il valore - <span class="codeph"> 1</span> indica che l'icona riappare a tempo indeterminato. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> sbiadire</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica la durata dell'animazione visualizzata o nascondere, in secondi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Nascondi automaticamente</span></span> </p> </td> 
   <td colname="col2"> <p> Imposta il numero di secondi in cui IconEffect rimane completamente visibile prima di nascondersi automaticamente. ovvero il tempo trascorso dopo il completamento della dissolvenza nell'animazione e prima dell'inizio dell'animazione di dissolvenza in uscita. Impostare questo valore su <span class="codeph"> 0</span> per disabilitare il comportamento di nascondere automatico. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
