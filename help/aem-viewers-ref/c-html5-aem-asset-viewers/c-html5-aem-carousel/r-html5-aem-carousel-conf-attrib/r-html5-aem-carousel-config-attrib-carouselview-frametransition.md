---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
TQID: 'https://experienceleague.adobe.com/65cLC5DOqdGrbVpMMy6gLBNL4F3WRqipNqIlpBIK-GM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 3%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`durata`*[, *`spaziatura`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nessuna|dissolvenza|diapositiva </span> </p> </td> 
   <td colname="col2"> <p>Specifica il tipo di effetto applicato al cambio di fotogramma. <span class="codeph"> none </span>, ad esempio, non rappresenta alcuna transizione; la modifica del frame avviene immediatamente. E, </p> <p> Dissolvenza </span> di <span class="codeph"> significa transizione di dissolvenza incrociata tra fotogrammi vecchi e nuovi. Infine, </p> <p> <span class="codeph"> diapositiva </span> attiva la transizione in cui il vecchio frame scorre fuori dalla visualizzazione e il nuovo frame scorre dentro. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durata </span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata (in secondi) dell'effetto di transizione </span> o <span class="codeph"> della dissolvenza </span> di <span class="codeph">. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spaziatura </span> </span> </p> </td> 
   <td colname="col2"> <p>La spaziatura tra fotogrammi adiacenti nella transizione </span> della diapositiva <span class="codeph"> ha un intervallo compreso tra <span class="codeph"> 0 </span> e <span class="codeph"> 1 </span> ed è relativa alla larghezza del componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

Nessuno.

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
