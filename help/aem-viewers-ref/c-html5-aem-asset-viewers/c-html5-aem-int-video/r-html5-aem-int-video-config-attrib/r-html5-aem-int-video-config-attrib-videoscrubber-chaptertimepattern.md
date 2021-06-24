---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: VideoScrubber.chaptertimepattern
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Developer,Business Practitioner
exl-id: 93c1d38c-1f45-4794-8084-f520f9caf257
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Attributo di configurazione per Visualizzatore video interattivo.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Imposta il pattern per l’ora visualizzata nella barra del titolo dell’etichetta del capitolo, in cui <span class="codeph"> h</span> rappresenta ore, <span class="codeph"> m</span> per minuti e <span class="codeph"> s</span> per secondi. </p> <p>Il numero di lettere utilizzato per ciascuna unità di tempo determina il numero di cifre da visualizzare per l'unità. Se il numero non può rientrare nelle cifre specificate, il valore equivalente viene visualizzato nell'unità successiva. </p> <p>Ad esempio, se l’ora corrente del filmato è 67 minuti e 5 secondi, un pattern di tempo di <span class="codeph"> m:ss</span> viene visualizzato come 67:05. La stessa ora viene visualizzata come 1:07:5 se il pattern di tempo è <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
chaptertimepattern=h:mm:ss
```
