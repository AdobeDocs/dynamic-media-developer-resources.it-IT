---
description: Attributo di configurazione per il visualizzatore Video360.
seo-description: Attributo di configurazione per il visualizzatore Video360.
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic media
uuid: fe145e6f-742e-44fc-b225-187a86b6700e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---


# VideoTime.timepattern{#videotime-timepattern}

Attributo di configurazione per il visualizzatore Video360.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Imposta il pattern per l'ora visualizzata nella barra di controllo, dove <span class="codeph"> h</span> è ore, <span class="codeph"> m</span> minuti e <span class="codeph"> s</span> secondi. </p> <p>Il numero di lettere utilizzato per ogni unità di tempo determina il numero di cifre da visualizzare per l'unità. Se il numero non può rientrare nelle cifre indicate, il valore equivalente viene visualizzato nell'unità successiva. </p> <p>Ad esempio, se l'ora corrente del filmato è 67 minuti e 5 secondi, il pattern di tempo <span class="codeph"> m:ss</span> è 67:05. La stessa ora viene visualizzata come 1:07:5 se il pattern di tempo specificato è <span class="codeph"> h:mm:s</span>. </p> </td> 
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

