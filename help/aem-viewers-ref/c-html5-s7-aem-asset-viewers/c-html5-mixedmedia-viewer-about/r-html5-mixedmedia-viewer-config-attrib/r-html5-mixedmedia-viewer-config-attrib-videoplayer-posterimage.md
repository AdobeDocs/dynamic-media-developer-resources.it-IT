---
title: VideoPlayer.posterimage
description: VideoPlayer.posterimage
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bcbba4c5-b758-4049-b4c2-f1c48cc2de7e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 2%

---

# VideoPlayer.posterimage{#videoplayer-posterimage}

` [VideoPlayer.|<containerId>_videoPlayer.]posterimage=none|[ *`image_id`*][? *`isCommands`*]`

<table id="table_AE7AAFA9B4374E31B51D06511EB96401"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nessuno|[<span class="varname"> image_id</span>][?<span class="varname"> isCommands</span>]</span> </p> </td> 
   <td colname="col2"> <p> Immagine da visualizzare sul primo fotogramma prima che inizi la riproduzione del video, risolta rispetto a <span class="codeph"> serverurl</span>. Se specificato nell’URL, codifica HTTP quanto segue: </p> <p> 
     <ul id="ul_B38A687CEFE64C68A0B2C227A68A458F"> 
      <li id="li_E7AE1BDAC17E49E0B7ACF89C5C0529F0"> <p> <span class="codeph"> ?</span> as <span class="codeph"> %3F</span> </p> </li> 
      <li id="li_391CCF067F734480B2B4AFC9760C479A"> <p> <span class="codeph"> E</span> as <span class="codeph"> %26</span> </p> </li> 
      <li id="li_6824B66A55554C5A8B12874DCF5BFAEE"> <p> <span class="codeph"> =</span> as <span class="codeph"> %3D</span> </p> </li> 
     </ul> </p> <p>Se il <span class="codeph"><span class="varname"> image_id</span></span> Se viene omesso, il componente tenta di utilizzare l’immagine copertina predefinita per quella risorsa. </p> <p>Quando il video viene specificato come percorso, l'ID di catalogo predefinito per le immagini poster viene derivato dal percorso del video come <span class="codeph"> catalog_id/image_id</span> coppia dove <span class="codeph"> catalog_id</span> corrisponde al primo token nel percorso. E, <span class="codeph"> image_id</span> è il nome del video con l’estensione rimossa. Se l'immagine con tale ID non esiste, l'immagine del poster non viene visualizzata. </p> <p>Per impedire la visualizzazione dell'immagine poster predefinita, specificare <span class="codeph"> nessuno</span> come valore dell’immagine del poster. Se solo il <span class="codeph"><span class="varname"> isCommands</span></span> vengono applicati all'immagine copertina predefinita prima che l'immagine venga visualizzata. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Nessuno.

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`posterimage=none`
