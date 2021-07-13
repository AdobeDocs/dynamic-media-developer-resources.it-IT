---
description: Dati a più bit rate.
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 3%

---

# mbrSet{#mbrset}

Dati a più bit rate.

`req=mbrSet[,text|xml[, *``*]][&fmt= *`encodingfmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

Restituisce un testo o una risposta xml che contiene un elenco di URL (e dei bit rate corrispondenti) corrispondenti a voci video valide nel set di video associato all&#39;ID del percorso netto.

Il precedente requisito per cui una voce video valida contiene un valore per `catalog::VideoBitRate` è stato semplificato. La voce può contenere un valore per `catalog::VideoBitRate`*o* `catalog::AudioBitRate`*o* `catalog::TotalStreamBitRate`. Per rendere valida la voce video, è necessario definire solo una di queste. Tieni presente che i requisiti per `catalog::Path` e un’estensione file video valida non sono cambiati.

Le risposte sono destinate al consumo da parte di Apple e Flash Streaming Server e sono quindi strutturalmente conformi a tali specifiche. Gli URL vengono generati utilizzando i prefissi `attribute::HttpAppleStreamingContext` e `attribute::HttpFlashStreamingContext`.

Le risposte m3u8 contengono solo file mp4 se presenti nel set video. Se non sono presenti file mp4, queste risposte contengono solo file f4v. Se non sono presenti file mp4 o f4v, la risposta è vuota.

Le risposte f4m contengono file f4v solo se sono presenti nel set di video. Se non sono presenti file f4v, queste risposte contengono solo file mp4. Se non sono presenti file f4v né file mp4, la risposta è vuota.

I bit rate visualizzati nelle risposte f4m/m3u8 corrispondono ai valori in `catalog::TotalStreamBitRate` (convertiti in unità appropriate). Se `catalog::TotalStreamBitRate` non è definito, viene utilizzata la somma di `catalog::VideoBitRate` e `catalog::AudioBitRate`.

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::NonImgExpiration`.
