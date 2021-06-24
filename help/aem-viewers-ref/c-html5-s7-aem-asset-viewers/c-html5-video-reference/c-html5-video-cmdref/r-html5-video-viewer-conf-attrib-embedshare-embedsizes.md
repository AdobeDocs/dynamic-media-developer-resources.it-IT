---
description: Attributo di configurazione per il visualizzatore video.
solution: Experience Manager
title: EmbedShare.embedsizes
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video
role: Developer,Business Practitioner
exl-id: cf075711-1275-4eb2-8cb6-fb2609711c7a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 10%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

Attributo di configurazione per il visualizzatore video.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *``*, *``*[,0|1][; *``*, *`larghezza larghezza altezza`*[,0|1]]`

Specifica un elenco di dimensioni da incorporare per la casella combinata dimensioni nella finestra di dialogo modale di condivisione da incorporare.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p> Larghezza da incorporare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height </span> </span> </p> </td> 
   <td colname="col2"> <p>Altezza da incorporare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Specifica se la voce dell'elenco deve essere inizialmente preselezionata nella casella combinata. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```
