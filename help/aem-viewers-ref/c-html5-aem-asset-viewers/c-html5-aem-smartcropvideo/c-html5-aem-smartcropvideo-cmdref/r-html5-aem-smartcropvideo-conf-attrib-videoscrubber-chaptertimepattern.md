---
title: VideoScrubber.chaptertimepattern
description: Attributo di configurazione per il visualizzatore video Ritaglio avanzato.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 5552ed9e-d8fe-4723-a360-405b91e27f8e
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 2%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Attributo di configurazione per il visualizzatore video Ritaglio avanzato.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Imposta il modello per il tempo visualizzato nella barra del titolo dell'etichetta del capitolo video. Le <span class="codeph"> h</span> sono ore, <span class="codeph"> m</span> sono minuti e <span class="codeph"> s</span> sono secondi. </p> <p>Il numero di lettere utilizzate per ciascuna unità di tempo determina il numero di cifre da visualizzare per l'unità. Se il numero non può rientrare nelle cifre specificate, il valore equivalente viene visualizzato nell’unità successiva. </p> <p>Ad esempio, se il tempo del filmato corrente è 67 minuti e 5 secondi, il modello di tempo <span class="codeph"> m:ss</span> verrà visualizzato come 67:05. La stessa ora viene visualizzata come 1:07:5 se il modello di ora specificato è <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
chaptertimepattern=h:mm:ss
```
