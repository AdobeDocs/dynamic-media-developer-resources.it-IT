---
description: Attributo di configurazione per il visualizzatore carosello.
seo-description: Attributo di configurazione per il visualizzatore carosello.
seo-title: CarouselView.autoplay
solution: Experience Manager
title: CarouselView.autoplay
topic: Dynamic media
uuid: 12730b17-110e-405b-97fe-e70fab89c703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CarouselView.autoplay{#carouselview-autoplay}

Attributo di configurazione per il visualizzatore carosello.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,durata][,direzione]</span> </p> </td> 
   <td colname="col2"> <p> Specifica l'attivazione/disattivazione, la durata di visualizzazione di ciascun banner nel carosello e la direzione del ciclo automatico. </p> <p>Impostare su <span class="codeph"> 0</span> per il ciclo automatico disattivato. </p> <p>Impostate <span class="codeph"> 1</span> per attivare il ciclo automatico con durata transizione in secondi controllata dalla <span class="codeph"> durata</span>. </p> <p>La direzione del ciclo automatico è controllata con <span class="codeph"> direzione</span>. La <span class="codeph"> direzione</span> è compresa tra <span class="codeph"> 1</span> da destra a sinistra e <span class="codeph"> 0</span> da sinistra a destra. </p> </td> 
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

