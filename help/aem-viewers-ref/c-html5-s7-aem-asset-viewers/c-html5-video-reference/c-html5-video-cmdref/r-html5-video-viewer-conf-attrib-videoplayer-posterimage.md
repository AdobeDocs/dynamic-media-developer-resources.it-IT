---
description: Attributo di configurazione per il visualizzatore video.
seo-description: Attributo di configurazione per il visualizzatore video.
seo-title: VideoPlayer.posterimage
solution: Experience Manager
title: VideoPlayer.posterimage
topic: Dynamic media
uuid: 59d81a72-ac17-4c32-ab47-89bd14dc17a5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.posterimage{#videoplayer-posterimage}

Attributo di configurazione per il visualizzatore video.

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_`*][? *`idisCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> L'immagine da visualizzare sul primo fotogramma prima dell'avvio della riproduzione del video, risolta in base al <span class="codeph"> server</span>. Se specificato nell’URL, codificate con HTTP quanto segue: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> come <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> come <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> come <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Se il valore <span class="codeph"><span class="varname"> image_id</span></span> viene omesso, il componente tenta di utilizzare l’immagine poster predefinita per tale risorsa. </p> <p>Quando il video viene specificato come percorso, l’ID predefinito del catalogo immagini poster viene derivato dal percorso video come coppia <span class="codeph"> catalog_id/image_id</span> , dove <span class="codeph"> catalog_id</span> corrisponde al primo token nel percorso e <span class="codeph"> image_id</span> è il nome del video con l’estensione rimossa. Se l'immagine con tale ID non esiste, l'immagine poster non viene visualizzata. </p> <p>Per impedire la visualizzazione dell'immagine poster predefinita, specificate <span class="codeph"> none</span> come valore dell'immagine poster. Se sono specificati solo i <span class="codeph"><span class="varname"> comandi</span></span> isCommands, i comandi vengono applicati all'immagine poster predefinita prima della visualizzazione dell'immagine. </p> </td> 
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

