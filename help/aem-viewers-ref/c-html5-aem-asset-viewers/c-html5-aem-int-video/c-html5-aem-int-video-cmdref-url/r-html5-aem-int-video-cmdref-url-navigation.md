---
description: Comando URL per il visualizzatore video interattivo.
seo-description: Comando URL per il visualizzatore video interattivo.
seo-title: navigazione
solution: Experience Manager
title: navigazione
uuid: eecc7458-153c-4f36-b29e-97451f275c0c
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 6%

---


# navigation{#navigation}

Comando URL per il visualizzatore video interattivo.

` navigation= *`file`*`

Il visualizzatore supporta la navigazione dei capitoli video tramite file WebVTT in hosting. Gli operatori di posizionamento dei cue non sono supportati.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un URL o un percorso per il contenuto di navigazione WebVTT. Image Server deve ospitare il file WebVTT. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

Nessuno.

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
navigation=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.navigation.vtt,1
```

