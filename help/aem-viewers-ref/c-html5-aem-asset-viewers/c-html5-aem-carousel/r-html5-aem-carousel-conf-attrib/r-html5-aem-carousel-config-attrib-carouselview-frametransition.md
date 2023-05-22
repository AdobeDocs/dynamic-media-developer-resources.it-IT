---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 4%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`durata`*[, *`spaziatura`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nessuno|dissolvenza|diapositiva </span> </p> </td> 
   <td colname="col2"> <p>Specifica il tipo di effetto applicato al cambio di fotogramma. Ad esempio: <span class="codeph"> nessuno </span> significa nessuna transizione; il cambiamento di fotogramma avviene immediatamente. E, </p> <p> <span class="codeph"> dissolvenza </span> significa transizione di dissolvenza incrociata tra i fotogrammi vecchi e nuovi. Infine, </p> <p> <span class="codeph"> diapositiva </span> attiva la transizione in cui il vecchio fotogramma scorre fuori dalla vista e il nuovo fotogramma scorre all'interno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durata </span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata (in secondi) di <span class="codeph"> dissolvenza </span> o <span class="codeph"> diapositiva </span> effetto di transizione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spaziatura </span> </span> </p> </td> 
   <td colname="col2"> <p>Spaziatura tra fotogrammi adiacenti in <span class="codeph"> diapositiva </span> transizione, ha l'intervallo tra <span class="codeph"> 0 </span> da a <span class="codeph"> 1 </span> ed è relativo alla larghezza del componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

Nessuno.

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
