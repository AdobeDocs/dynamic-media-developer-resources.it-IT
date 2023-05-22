---
title: VideoScrubber.timepattern
description: VideoScrubber.timepattern
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0536110e-a885-4fd4-baa8-742fcdba5cc9
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 2%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_D1D7BE09311B469983B52E34338FEAFE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Imposta il modello per la visualizzazione del tempo nell'indicatore del tempo, dove <span class="codeph"> h</span> è ore, <span class="codeph"> m</span> è in minuti, e <span class="codeph"> s</span> è di secondi. </p> <p>Il numero di lettere utilizzate per ciascuna unità di tempo determina il numero di cifre da visualizzare per l'unità. Se il numero non può rientrare nelle cifre specificate, il valore equivalente viene visualizzato nell’unità successiva. </p> <p>Ad esempio, se il tempo del filmato corrente è di 67 minuti e 5 secondi, il modello di tempo <span class="codeph"> m:ss</span> viene visualizzato come 67:05. Viene visualizzata la stessa ora come 1:07:5 se il modello di tempo specificato è <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
