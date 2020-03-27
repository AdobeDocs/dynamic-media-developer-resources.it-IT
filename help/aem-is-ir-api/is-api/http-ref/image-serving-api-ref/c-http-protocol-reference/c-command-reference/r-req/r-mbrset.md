---
description: Dati con bitrate multiplo.
seo-description: Dati con bitrate multiplo.
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mbrSet{#mbrset}

Dati con bitrate multiplo.

`req=mbrSet[,text|xml[, *``*]][&fmt= *`encodingfmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m| m3u8</span> </p></td> 
 </tr> 
</table>

Restituisce una risposta di testo o xml che contiene un elenco di URL (e di bitrate corrispondenti) che corrispondono a voci video valide in set di video associate all’ID del percorso di rete.

Il precedente requisito per cui una voce video valida contiene un valore per `catalog::VideoBitRate` è ora stato semplificato. La voce può contenere un valore per `catalog::VideoBitRate`*o *`catalog::AudioBitRate`*o* `catalog::TotalStreamBitRate`. Affinché la voce video sia valida, è necessario definire solo una di queste opzioni. Tenete presente che i requisiti per `catalog::Path` e un’estensione file video valida non sono cambiati.

Le risposte sono destinate al consumo da parte dei server di streaming Apple e Flash e sono quindi strutturalmente conformi a tali specifiche. Gli URL vengono generati utilizzando prefissi `attribute::HttpAppleStreamingContext` e `attribute::HttpFlashStreamingContext`.

Le risposte m3u8 contengono solo file mp4 se presenti nel set video. Se non sono presenti file mp4, queste risposte contengono solo file f4v. Se non sono presenti file mp4 o f4v, la risposta è vuota.

Le risposte f4m contengono solo file f4v se sono presenti nel set video. Se non sono presenti file f4v, queste risposte contengono solo file mp4. Se non sono presenti file f4v né file mp4, la risposta è vuota.

I bitrate visualizzati nelle risposte f4m/m3u8 corrispondono ai valori in `catalog::TotalStreamBitRate` (convertiti in unità appropriate). Se non `catalog::TotalStreamBitRate` è definito, viene utilizzata la somma di `catalog::VideoBitRate` e `catalog::AudioBitRate` .

La risposta HTTP può essere memorizzata nella cache con TTL basato su `catalog::NonImgExpiration`.
