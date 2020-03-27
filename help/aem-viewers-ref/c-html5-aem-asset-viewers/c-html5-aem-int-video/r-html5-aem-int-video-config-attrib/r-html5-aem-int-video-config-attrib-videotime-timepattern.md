---
description: Attributo di configurazione per il visualizzatore video interattivo.
seo-description: Attributo di configurazione per il visualizzatore video interattivo.
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic media
uuid: 90d36f73-44f9-4e4e-9ad6-e866749f9b2f
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# VideoTime.timepattern{#videotime-timepattern}

Attributo di configurazione per il visualizzatore video interattivo.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Imposta il pattern per il tempo visualizzato nella barra di controllo, dove <span class="codeph"> h</span> rappresenta ore, <span class="codeph"> m</span> per minuti e <span class="codeph"> s</span> per secondi. </p> <p>Il numero di lettere utilizzato per ogni unità di tempo determina il numero di cifre da visualizzare per l'unità. Se il numero non può rientrare nelle cifre indicate, il valore equivalente viene visualizzato nell'unità successiva. </p> <p>Ad esempio, se l’ora corrente del filmato è 67 minuti e 5 secondi, un pattern di tempo di <span class="codeph"> m:ss</span> viene visualizzato come 67:05. La stessa ora viene visualizzata come 1:07:5 se il pattern di tempo è <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```

