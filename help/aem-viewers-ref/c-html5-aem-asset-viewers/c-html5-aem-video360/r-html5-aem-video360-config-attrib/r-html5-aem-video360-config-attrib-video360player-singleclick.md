---
description: Attributo di configurazione per il visualizzatore Video360.
solution: Experience Manager
title: Video360Player.singleclick
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video VR 360
role: Developer,Business Practitioner
exl-id: dfb44ed5-5f4f-4a2c-a3b4-d49502556399
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

---

# Video360Player.singleclick{#video-player-singleclick}

Attributo di configurazione per il visualizzatore Video360.

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

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
