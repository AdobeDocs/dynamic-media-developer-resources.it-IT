---
title: CarouselView.autoplay
description: Attributo di configurazione per visualizzatore carosello.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# CarouselView.autoplay{#carouselview-autoplay}

Attributo di configurazione per visualizzatore carosello.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duration][,direzione]</span> </p> </td> 
   <td colname="col2"> <p> Specifica l'attivazione/disattivazione, la durata di visualizzazione di ogni banner nel carosello e la direzione del ciclo automatico. </p> <p>Impostato su <span class="codeph"> 0</span> per disattivare il ciclo automatico. </p> <p>Imposta <span class="codeph"> 1</span> per attivare il ciclo automatico con durata di transizione in secondi controllata da <span class="codeph"> duration</span>. </p> <p>La direzione del ciclo automatico è controllata con <span class="codeph"> direzione</span>. La direzione <span class="codeph"></span> ha un intervallo compreso tra <span class="codeph"> 1</span> da destra a sinistra e <span class="codeph"> 0</span> da sinistra a destra. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1,9`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```
