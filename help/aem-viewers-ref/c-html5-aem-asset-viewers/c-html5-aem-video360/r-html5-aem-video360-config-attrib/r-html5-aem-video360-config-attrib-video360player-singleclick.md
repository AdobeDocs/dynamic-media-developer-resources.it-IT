---
description: Attributo di configurazione per il visualizzatore Video360.
seo-description: Attributo di configurazione per il visualizzatore Video360.
seo-title: Video360Player.singleclick
solution: Experience Manager
title: Video360Player.singleclick
topic: Dynamic media
uuid: 2972405c-5c89-45d0-a542-19c7463901b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 12%

---


# Video360Player.singleclick{#video-player-singleclick}

Attributo di configurazione per il visualizzatore Video360.

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura del singolo clic/tocco per attivare/disattivare la riproduzione/pausa. Se si imposta su <span class="codeph"> none</span>, il tocco o il clic singolo viene disattivato per la riproduzione o la pausa. Se è impostato su <span class="codeph"> playPause</span>, facendo clic sul video si passa dalla riproduzione alla pausa. Su alcuni dispositivi è possibile utilizzare i controlli nativi. In questo caso, un comportamento <span class="codeph"> singleclick</span> è disabilitato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`playPause`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```

