---
title: CarouselView.enableHD
description: CarouselView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 4%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`numero`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Abilita, limita o disabilita l'ottimizzazione per i dispositivi in cui <span class="codeph"> devicePixelRatio</span> è maggiore di <span class="codeph"> 1</span>, ovvero per i dispositivi con visualizzazione ad alta densità come iPhone4 e dispositivi simili. </p> <p>Se attivo, il componente limita le dimensioni della richiesta di immagine IS come se il dispositivo avesse solo un rapporto di pixel di <span class="codeph"> 1</span> e in questo modo riducesse la larghezza di banda. </p> <p>Vedi l'esempio seguente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> numero</span></span> </p> </td> 
   <td colname="col2"> <p> Se si utilizza l'impostazione <span class="codeph"> limit</span> , il componente attiva una densità di pixel elevata solo fino al limite specificato. </p> <p>Vedi l'esempio seguente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
