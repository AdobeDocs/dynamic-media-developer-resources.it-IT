---
description: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
topic: Dynamic media
uuid: 0dcebbce-f449-4f5f-acbc-02960e1dbdba
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 6%

---


# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> precaricatore</span></span> </p> </td> 
   <td> <p>Specifica il comportamento di precaricamento del componente. </p> <p>Se impostato su <span class="codeph"> -1</span>, il componente precarica tutti i fotogrammi del carosello quando è in stato di inattività. </p> <p>Se impostato su <span class="codeph"> 0</span>, il componente carica solo il fotogramma attualmente visibile, precedente e successivo. </p> <p><span class="codeph"><span class="varname"> Il </span></span>precaricamento definisce quanti fotogrammi invisibili intorno al fotogramma attualmente visualizzato vengono precaricati se in stato di inattività. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
