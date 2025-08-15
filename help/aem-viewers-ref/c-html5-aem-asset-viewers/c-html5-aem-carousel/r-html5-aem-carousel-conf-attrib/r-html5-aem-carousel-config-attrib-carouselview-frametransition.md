---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`durata`*[, *`spaziatura`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nessuna|dissolvenza|diapositiva </span> </p> </td> 
   <td colname="col2"> <p>Specifica il tipo di effetto applicato al cambio di fotogramma. <span class="codeph"> none </span>, ad esempio, non rappresenta alcuna transizione; la modifica del frame avviene immediatamente. E, </p> <p> Dissolvenza <span class="codeph"> di </span> significa transizione di dissolvenza incrociata tra fotogrammi vecchi e nuovi. Infine, </p> <p> <span class="codeph"> diapositiva </span> attiva la transizione in cui il vecchio frame scorre fuori dalla visualizzazione e il nuovo frame scorre dentro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durata </span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata (in secondi) dell'effetto di transizione <span class="codeph"> o </span> della dissolvenza <span class="codeph"> di </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spaziatura </span> </span> </p> </td> 
   <td colname="col2"> <p>La spaziatura tra fotogrammi adiacenti nella transizione <span class="codeph"> della diapositiva </span> ha un intervallo compreso tra <span class="codeph"> 0 </span> e <span class="codeph"> 1 </span> ed è relativa alla larghezza del componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

Nessuno.

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
