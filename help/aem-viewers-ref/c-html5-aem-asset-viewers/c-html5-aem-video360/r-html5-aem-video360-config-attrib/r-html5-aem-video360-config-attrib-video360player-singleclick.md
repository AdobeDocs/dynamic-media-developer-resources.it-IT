---
title: Video360Player.singleclick
description: Attributo di configurazione per il visualizzatore Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: dfb44ed5-5f4f-4a2c-a3b4-d49502556399
TQID: 'https://experienceleague.adobe.com/PDAYnwkhHXn-JgGfsIqvDxYhQ3LiXLGqtCgRK-CPq3A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 4%

---

# Video360Player.singleclick{#video-player-singleclick}

Attributo di configurazione per il visualizzatore Video360.

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura di clic/tocco per riprodurre e mettere in pausa. L'impostazione su <span class="codeph"> none</span> disattiva il clic/tocco per riprodurre/mettere in pausa. Se è impostato su <span class="codeph"> playPause</span>, la selezione del video consente di alternare la riproduzione e la messa in pausa del video. Su alcuni dispositivi è possibile utilizzare i controlli nativi. In questo caso, un comportamento <span class="codeph"> singleclick</span> è disabilitato. </p> </td> 
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
