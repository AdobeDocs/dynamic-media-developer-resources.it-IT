---
title: VideoPlayer.posterimage
description: VideoPlayer.posterimage
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bcbba4c5-b758-4049-b4c2-f1c48cc2de7e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nessuno|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Immagine da visualizzare sul primo fotogramma prima dell'inizio della riproduzione del video, risolta rispetto a <span class="codeph"> serverurl</span>. Se specificato nell’URL, codifica HTTP quanto segue: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph">?</span> come <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> &amp;</span> come <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> come <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Se il valore <span class="codeph"><span class="varname"> image_id</span></span> viene omesso, il componente tenta di utilizzare l'immagine copertina predefinita per quella risorsa. </p> <p>Quando il video viene specificato come percorso, l'ID del catalogo immagini poster predefinito deriva dal percorso del video come coppia <span class="codeph"> catalog_id/image_id</span> in cui <span class="codeph"> catalog_id</span> corrisponde al primo token nel percorso. E <span class="codeph"> image_id</span> è il nome del video con estensione rimossa. Se l'immagine con tale ID non esiste, l'immagine del poster non viene visualizzata. </p> <p>Per impedire la visualizzazione dell'immagine poster predefinita, specificare <span class="codeph"> none</span> come valore dell'immagine poster. Se vengono specificati solo i comandi isCommands<span class="codeph"><span class="varname"> di </span></span>, i comandi vengono applicati all'immagine copertina predefinita prima della visualizzazione dell'immagine. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Nessuno.

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
