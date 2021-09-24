---
title: interattiva
description: Comando URL per il visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 5%

---

# interattiva{#interactivedata}

Comando URL per il visualizzatore video interattivo.

`interactivedata= *`file`*`

I dati interattivi associano determinate aree temporali nel contenuto video ai dati del prodotto visualizzati in seguito nei campioni interattivi accanto al video. È inoltre associato nel pannello di invito all’azione mostrato al termine della riproduzione video. Fornisce inoltre un titolo per il video interattivo visualizzato nel pannello di invito all’azione.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un URL o un percorso per il contenuto di dati interattivi WebVTT. Il file WebVTT deve essere gestito da Image Server. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

Nessuno.

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
interactivedata=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt
```
