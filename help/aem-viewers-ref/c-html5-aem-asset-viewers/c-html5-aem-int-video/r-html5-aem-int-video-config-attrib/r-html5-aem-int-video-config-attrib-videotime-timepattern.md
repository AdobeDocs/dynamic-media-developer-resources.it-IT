---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: VideoTime.timepattern
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
exl-id: de071adf-6c3c-4702-8950-8246b8ee459e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# VideoTime.timepattern{#videotime-timepattern}

Attributo di configurazione per Visualizzatore video interattivo.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Imposta il pattern per l’ora visualizzata nella barra dei controlli, in cui <span class="codeph"> h</span> rappresenta ore, <span class="codeph"> m</span> minuti e <span class="codeph"> s</span> per secondi. </p> <p>Il numero di lettere utilizzato per ciascuna unità di tempo determina il numero di cifre da visualizzare per l'unità. Se il numero non può rientrare nelle cifre specificate, il valore equivalente viene visualizzato nell'unità successiva. </p> <p>Ad esempio, se l’ora corrente del filmato è 67 minuti e 5 secondi, un pattern di tempo di <span class="codeph"> m:ss</span> viene visualizzato come 67:05. La stessa ora viene visualizzata come 1:07:5 se il pattern di tempo è <span class="codeph"> h:mm:s</span>. </p> </td> 
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
