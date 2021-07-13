---
description: Attributo di configurazione per il visualizzatore Carosello.
solution: Experience Manager
title: CarouselView.autoplay
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# CarouselView.autoplay{#carouselview-autoplay}

Attributo di configurazione per il visualizzatore Carosello.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,durata][,direzione]</span> </p> </td> 
   <td colname="col2"> <p> Specifica l'attivazione/disattivazione, la durata di visualizzazione di ciascun banner nel carosello e la direzione del ciclo automatico. </p> <p>Impostare su <span class="codeph"> 0</span> per il ciclo automatico disattivato. </p> <p>Imposta <span class="codeph"> 1</span> per l'attivazione automatica del ciclo con la durata della transizione in secondi controllata da <span class="codeph"> duration</span>. </p> <p>La direzione del ciclo automatico è controllata con <span class="codeph"> direzione</span>. La <span class="codeph"> direzione</span> ha un intervallo compreso tra <span class="codeph"> 1</span> da destra a sinistra e <span class="codeph"> 0</span> da sinistra a destra. </p> </td> 
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
