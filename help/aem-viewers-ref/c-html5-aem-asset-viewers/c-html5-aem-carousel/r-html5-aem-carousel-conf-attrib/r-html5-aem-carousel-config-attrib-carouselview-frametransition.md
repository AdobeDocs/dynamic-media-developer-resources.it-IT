---
description: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Developer,Business Practitioner
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 5%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`spaziatura tra le durate`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|dissolvenza|diapositiva  </span> </p> </td> 
   <td colname="col2"> <p>Specifica il tipo di effetto applicato alla modifica del fotogramma. <span class="codeph"> nessuno  </span> significa nessuna transizione; il cambiamento avviene all'istante. </p> <p> <span class="codeph"> dissolvenza  </span> significa transizione in dissolvenza incrociata tra fotogrammi vecchi e nuovi. </p> <p> <span class="codeph"> La diapositiva  </span> attiva la transizione in cui la vecchia cornice scorre dalla vista e la nuova cornice si trova. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durata  </span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata (in secondi) dell'effetto di transizione <span class="codeph"> dissolvenza </span> o <span class="codeph"> diapositiva </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spaziatura  </span> </span> </p> </td> 
   <td colname="col2"> <p>La spaziatura tra fotogrammi adiacenti nella transizione <span class="codeph"> diapositiva </span>, ha l'intervallo tra <span class="codeph"> 0 </span> e <span class="codeph"> 1 </span> ed è relativa alla larghezza del componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

Nessuno.

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
