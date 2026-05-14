---
title: SmartCropVideoPlayer.posterimage
description: Attributo di configurazione per il visualizzatore video Ritaglio avanzato.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: ff4f8e2c-b9c3-4fba-b3f0-fa1eaddcd8c0
TQID: 'https://experienceleague.adobe.com/tTBGmii-taSeo6W1AZ9CtgEpW6jFObLUTLsNiYgvOrA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 173
ht-degree: 1%

---

# SmartCropVideoPlayer.posterimage{#smartcropvideoplayer-posterimage}

Attributo di configurazione per il visualizzatore video Ritaglio avanzato.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nessuno|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Immagine da visualizzare sul primo fotogramma prima dell'inizio della riproduzione del video, risolta rispetto a <span class="codeph"> serverurl</span>. Se specificato nell’URL, codifica HTTP quanto segue: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> come <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> come <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> come <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Se il valore <span class="codeph"><span class="varname"> image_id</span></span> viene omesso, il componente tenta di utilizzare l'immagine copertina predefinita per quella risorsa. </p> <p>Quando il video viene specificato come percorso, l'ID catalogo predefinito per le immagini poster deriva dal percorso video come coppia <span class="codeph"> catalog_id/image_id</span>. Il <span class="codeph"> catalog_id</span> corrisponde al primo token nel percorso e <span class="codeph"> image_id</span> è il nome del video con estensione rimossa. Se l'immagine con tale ID non esiste, l'immagine del poster non viene visualizzata. </p> <p>Per impedire la visualizzazione dell'immagine poster predefinita, specificare <span class="codeph"> none</span> come valore dell'immagine poster. Se vengono specificati solo i comandi isCommands</span></span> di <span class="codeph"><span class="varname">, i comandi vengono applicati all'immagine copertina predefinita prima della visualizzazione dell'immagine. </p> </td> 
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
