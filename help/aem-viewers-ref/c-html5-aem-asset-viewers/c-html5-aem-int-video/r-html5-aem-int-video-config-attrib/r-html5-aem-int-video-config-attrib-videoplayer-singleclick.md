---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Developer,User
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Attributo di configurazione per Visualizzatore video interattivo.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura di un singolo clic/tocco per attivare/disattivare la riproduzione/pausa. Impostando su <span class="codeph"> none</span> si disattiva il tocco o il clic singolo per riprodurre/mettere in pausa. Se è impostato su <span class="codeph"> playPause</span>, facendo clic sul video si passa dalla riproduzione alla messa in pausa. Su alcuni dispositivi è possibile utilizzare controlli nativi. In questo caso, un comportamento <span class="codeph"> singleclick</span> è disabilitato. </p> </td> 
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
