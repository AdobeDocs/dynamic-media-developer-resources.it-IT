---
description: VideoScrubber.timepattern
solution: Experience Manager
title: VideoScrubber.timepattern
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# VideoScrubber.timepattern{#videoscrubber-timepattern}

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_D1D7BE09311B469983B52E34338FEAFE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Imposta il pattern per l’ora visualizzata nella bolla temporale in cui <span class="codeph"> h</span> è ore, <span class="codeph"> m</span> è minuti e <span class="codeph"> s</span> è secondi. </p> <p>Il numero di lettere utilizzato per ciascuna unità di tempo determina il numero di cifre da visualizzare per l'unità. Se il numero non può rientrare nelle cifre specificate, il valore equivalente viene visualizzato nell'unità successiva. </p> <p>Ad esempio, se l’ora corrente del filmato è 67 minuti e 5 secondi, il pattern di tempo <span class="codeph"> m:ss</span> è 67:05. La stessa ora viene visualizzata come 1:07:5 se il pattern di tempo specificato è <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
