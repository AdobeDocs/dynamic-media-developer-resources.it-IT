---
description: Dati a velocità multi-bit.
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# mbrSet{#mbrset}

Dati a velocità multi-bit.

`req=mbrSet[,text|xml[, *`codifica`*]][&fmt= *`fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codifica</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

Restituisce una risposta in formato testo o xml contenente un elenco di URL (con le velocità bit corrispondenti) corrispondenti alle voci video valide nel set di video associate all&#39;ID percorso netto.

Il precedente requisito che una voce video valida contenga un valore per `catalog::VideoBitRate` è stato reso meno rigido. La voce può contenere un valore per `catalog::VideoBitRate`*or* `catalog::AudioBitRate`*or* `catalog::TotalStreamBitRate`. Affinché la voce video sia valida, è necessario definire solo una di queste impostazioni. I requisiti per `catalog::Path` e un&#39;estensione di file video valida non sono stati modificati.

Le risposte sono destinate all’utilizzo da parte di Apple e dei server di streaming di Flash e sono quindi strutturalmente conformi a tali specifiche. Gli URL vengono generati utilizzando i prefissi `attribute::HttpAppleStreamingContext` e `attribute::HttpFlashStreamingContext`.

le risposte m3u8 contengono solo file mp4 se presenti nel set di video. Se non sono presenti file mp4, queste risposte contengono solo file f4v. Se non sono presenti file mp4 né file f4v, la risposta è vuota.

Le risposte f4m contengono solo file f4v se presenti nel set di video. Se non sono presenti file f4v, queste risposte contengono solo file mp4. Se non sono presenti file f4v né file mp4, la risposta è vuota.

I bit rate visualizzati nelle risposte f4m/m3u8 corrispondono ai valori in `catalog::TotalStreamBitRate` (convertiti in unità appropriate). Se `catalog::TotalStreamBitRate` non è definito, viene utilizzata la somma di `catalog::VideoBitRate` e `catalog::AudioBitRate`.

La risposta HTTP è memorizzabile in cache con TTL basato su `catalog::NonImgExpiration`.
