---
title: VideoPlayer.posterimage
description: Attributo di configurazione per il visualizzatore video.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: c09884e2-60a1-4fce-997a-29747b4ccb7b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

Attributo di configurazione per il visualizzatore video.

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isControls`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nessuno|[<span class="varname"> image_id</span>][?<span class="varname"> isControls</span>]</span> </p> </td> 
   <td colname="col2"> <p> Immagine da visualizzare sul primo fotogramma prima dell'inizio della riproduzione del video, risolta contro <span class="codeph"> serverurl</span>. Se specificato nell’URL, codifica HTTP come segue: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> come <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> come <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> come <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Se la <span class="codeph"><span class="varname"> image_id</span></span> viene omesso, il componente tenta di utilizzare l'immagine poster predefinita per la risorsa. </p> <p>Quando il video è specificato come percorso, l’ID catalogo predefinito delle immagini miniatura viene derivato dal percorso video come <span class="codeph"> catalog_id/image_id</span> coppia dove <span class="codeph"> catalog_id</span> corrisponde al primo token nel percorso. E <span class="codeph"> image_id</span> è il nome del video con l'estensione rimossa. Se l'immagine con quell'ID non esiste, l'immagine poster non viene visualizzata. </p> <p>Per impedire la visualizzazione dell'immagine poster predefinita, specifica <span class="codeph"> nessuno</span> come valore dell'immagine poster. Se solo la <span class="codeph"><span class="varname"> isControls</span></span> i comandi vengono applicati all'immagine poster predefinita prima della visualizzazione dell'immagine. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

Nessuno.

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
posterimage=none
```
