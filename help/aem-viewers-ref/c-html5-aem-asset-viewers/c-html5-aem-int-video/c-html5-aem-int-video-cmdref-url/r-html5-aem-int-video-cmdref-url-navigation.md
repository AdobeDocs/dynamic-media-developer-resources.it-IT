---
description: Comando URL per il visualizzatore video interattivo.
solution: Experience Manager
title: navigazione
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 7%

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

