---
title: VideoTime.timepattern
description: Attributo di configurazione per Visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 1fe2876c-c59a-4e0c-b429-34cc3244d920
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 2%

---

# VideoTime.timepattern{#videotime-timepattern}

Attributo di configurazione per Visualizzatore video.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Imposta il modello per il tempo visualizzato nella barra di controllo, dove <span class="codeph"> h</span> è ore, <span class="codeph"> m</span> è in minuti, e <span class="codeph"> s</span> è di secondi. </p> <p>Il numero di lettere utilizzate per ciascuna unità di tempo determina il numero di cifre da visualizzare per l'unità. Se il numero non può rientrare nelle cifre specificate, il valore equivalente viene visualizzato nell’unità successiva. </p> <p>Ad esempio, se il tempo del filmato corrente è di 67 minuti e 5 secondi, il modello di tempo <span class="codeph"> m:ss</span> viene visualizzato come 67:05. Viene visualizzata la stessa ora come 1:07:5 se il modello di tempo specificato è <span class="codeph"> h:mm:s</span>. </p> </td> 
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
