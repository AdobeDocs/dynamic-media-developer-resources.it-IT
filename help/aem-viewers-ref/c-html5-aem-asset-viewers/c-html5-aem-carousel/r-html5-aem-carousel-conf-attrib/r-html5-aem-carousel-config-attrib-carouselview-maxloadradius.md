---
description: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
uuid: 0dcebbce-f449-4f5f-acbc-02960e1dbdba
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---


# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> precaricare</span></span> </p> </td> 
   <td> <p>Specifica il comportamento di precaricamento del componente. </p> <p>Se è impostato su <span class="codeph"> -1</span>, il componente precarica tutti i fotogrammi del carosello quando è in uno stato di inattività. </p> <p>Se è impostato su <span class="codeph"> 0</span> il componente carica solo il fotogramma attualmente visibile, precedente e successivo. </p> <p><span class="codeph"><span class="varname"> </span></span>precaricamento definisce quanti fotogrammi invisibili intorno al fotogramma attualmente visualizzato vengono precaricati quando si trova in uno stato di inattività. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
