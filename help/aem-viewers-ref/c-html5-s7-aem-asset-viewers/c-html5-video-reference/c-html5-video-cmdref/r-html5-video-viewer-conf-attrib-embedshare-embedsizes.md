---
description: Attributo di configurazione per il visualizzatore video.
seo-description: Attributo di configurazione per il visualizzatore video.
seo-title: EmbedShare.embedsize
solution: Experience Manager
title: EmbedShare.embedsize
topic: Dynamic media
uuid: 1fc6057f-9e25-4e94-b516-e3e7af60188c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# EmbedShare.embedsize{#embedshare-embedsizes}

Attributo di configurazione per il visualizzatore video.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`larghezza`*, *``*[,0|1][; *``*, *`altezza larghezza`*[,0|1]]`

Specifica un elenco di dimensioni di incorporamento per la casella combinata delle dimensioni nella finestra di dialogo modale di condivisione incorpora.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p> Incorpora larghezza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height </span> </span> </p> </td> 
   <td colname="col2"> <p>Incorpora altezza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Specifica se la voce di elenco deve essere inizialmente preselezionata nella casella combinata. </p> </td> 
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

