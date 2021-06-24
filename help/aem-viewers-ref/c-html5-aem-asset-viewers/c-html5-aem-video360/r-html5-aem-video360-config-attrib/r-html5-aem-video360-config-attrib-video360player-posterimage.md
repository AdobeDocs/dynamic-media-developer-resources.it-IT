---
description: Attributo di configurazione per il visualizzatore Video360.
solution: Experience Manager
title: Video360Player.posterimage
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video VR 360
role: Developer,Business Practitioner
exl-id: fffd0976-0aeb-4e61-981f-b84e9076f35f
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 12%

---

# Video360Player.posterimage{#video-player-posterimage}

Attributo di configurazione per il visualizzatore Video360.

` [Video360Player.|<containerId>_video360Player.]posterimage=none|[? *`isControls`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|[?<span class="varname"> isControls</span>]</span> </p> </td> 
   <td colname="col2"> <p> Modificatori Image Serving che controllano l'aspetto dell'immagine poster. Se specificato nell’URL, codifica HTTP come segue: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> come  <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> come  <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> come  <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p> Questo modificatore funziona per il contenuto video in hosting su Dynamic Media Classic o AEM Dynamic Media. </p> <p>Per impedire la visualizzazione dell'immagine poster predefinita, specifica <span class="codeph"> none</span> come valore dell'immagine poster. </p> </td> 
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
