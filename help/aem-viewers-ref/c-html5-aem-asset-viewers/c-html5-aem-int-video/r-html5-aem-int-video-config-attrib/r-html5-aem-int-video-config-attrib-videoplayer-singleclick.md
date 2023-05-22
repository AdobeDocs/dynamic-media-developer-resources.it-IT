---
title: VideoPlayer.singleclick
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Attributo di configurazione per Visualizzatore video interattivo.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura di clic/tocco per riprodurre e mettere in pausa. Impostazione di <span class="codeph"> nessuno</span> disabilita il clic/tocco per riprodurre/mettere in pausa. Se impostato su <span class="codeph"> playPause</span>, quindi selezionando il video si passa dalla riproduzione alla sospensione del video. Su alcuni dispositivi è possibile utilizzare i controlli nativi. In questo caso, un <span class="codeph"> singleclick</span> il comportamento è disabilitato. </p> </td> 
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
