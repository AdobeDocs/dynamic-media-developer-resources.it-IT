---
description: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Developer,Business Practitioner
exl-id: 0c79b3e2-ac5a-43c3-ac52-8240e7ed3cc1
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Imposta il pattern per l’ora visualizzata nella barra dei controlli, dove <span class="codeph"> h</span> è ore, <span class="codeph"> m</span> è minuti e <span class="codeph"> s</span> è secondi. </p> <p>Il numero di lettere utilizzato per ciascuna unità di tempo determina il numero di cifre da visualizzare per l'unità. Se il numero non può rientrare nelle cifre specificate, il valore equivalente viene visualizzato nell'unità successiva. </p> <p>Ad esempio, se l’ora corrente del filmato è 67 minuti e 5 secondi, il pattern di tempo <span class="codeph"> m:ss</span> è 67:05. La stessa ora viene visualizzata come 1:07:5 se il pattern di tempo specificato è <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
