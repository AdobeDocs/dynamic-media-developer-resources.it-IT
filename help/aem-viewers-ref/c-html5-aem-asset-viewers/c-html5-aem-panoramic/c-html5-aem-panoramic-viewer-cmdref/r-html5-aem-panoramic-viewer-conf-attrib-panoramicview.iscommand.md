---
title: PanoramicView.iscommand
description: Attributo di configurazione per visualizzatore panoramico.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# PanoramicView.iscommand{#panoramicview-iscommand}

Attributo di configurazione per visualizzatore panoramico.

` [PanoramicView.|<containerId>_panoramicView.]iscommand=isCommand `

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Stringa di comando Image Server applicata all'immagine.  Se è specificato nell’URL, assicurati di codificare tutte le occorrenze di <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> come <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>, rispettivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>


## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

Nessuna impostazione predefinita.

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Se specificato nell’URL del visualizzatore.

```
iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000
```

Se specificato nei dati di configurazione.

```
iscommand=op_sharpen=1&op_colorize=0xff0000
```
