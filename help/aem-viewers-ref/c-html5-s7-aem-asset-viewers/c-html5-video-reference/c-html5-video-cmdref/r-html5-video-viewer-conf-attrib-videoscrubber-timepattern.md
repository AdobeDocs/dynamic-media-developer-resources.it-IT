---
title: VideoScrubber.timepattern
description: Attributo di configurazione per il visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e0956a0b-4d82-475f-8990-8b059014233a
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

Attributo di configurazione per il visualizzatore video.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Imposta il pattern per l’ora visualizzata nella bolla temporale, dove <span class="codeph"> h</span> è ore, <span class="codeph"> m</span> è in minuti e <span class="codeph"> s</span> è in secondi. </p> <p>Il numero di lettere utilizzato per ciascuna unità di tempo determina il numero di cifre da visualizzare per l'unità. Se il numero non può rientrare nelle cifre specificate, il valore equivalente viene visualizzato nell'unità successiva. </p> <p>Ad esempio, se l’ora corrente del filmato è 67 minuti e 5 secondi, il pattern di tempo <span class="codeph"> m:ss</span> mostra come 67:05. La stessa ora viene visualizzata come 1:07:5 se il modello temporale specificato è <span class="codeph"> h:mm:s</span>. </p> </td> 
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
