---
description: Attributo di configurazione per il visualizzatore video.
seo-description: Attributo di configurazione per il visualizzatore video.
seo-title: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
topic: Dynamic media
uuid: 44c86fdb-7e96-4d90-99a1-3b0670d3696f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

Attributo di configurazione per il visualizzatore video.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Imposta il pattern per l'ora visualizzata nella bolla temporale in cui <span class="codeph"> h</span> è ore, <span class="codeph"> m</span> è di minuti e <span class="codeph"> s</span> di secondi. </p> <p>Il numero di lettere utilizzato per ogni unità di tempo determina il numero di cifre da visualizzare per l'unità. Se il numero non può rientrare nelle cifre indicate, il valore equivalente viene visualizzato nell'unità successiva. </p> <p>Ad esempio, se l'ora corrente del filmato è 67 minuti e 5 secondi, il pattern di tempo <span class="codeph"> m:ss</span> è 67:05. La stessa ora viene visualizzata come 1:07:5 se il pattern di tempo specificato è <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```

