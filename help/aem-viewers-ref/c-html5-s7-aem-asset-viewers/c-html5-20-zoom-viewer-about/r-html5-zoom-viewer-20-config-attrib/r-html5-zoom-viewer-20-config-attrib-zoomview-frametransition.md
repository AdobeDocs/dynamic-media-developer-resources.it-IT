---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.frametransition
solution: Experience Manager
title: ZoomView.frametransition
topic: Dynamic media
uuid: 28e283ca-51d8-4d6c-9b8a-d16da21f4da1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 5%

---


# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *``*[, *`durata`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide  </span> </p> </td> 
   <td colname="col2"> <p>Specifica il tipo di effetto applicato alla modifica del fotogramma. <span class="codeph"> none non  </span> significa nessuna transizione;, il cambiamento di fotogramma avviene all’istante. <span class="codeph"> dissolvenza  </span> significa transizione in dissolvenza incrociata tra i fotogrammi vecchi e nuovi. <span class="codeph"> diapositiva  </span> attiva la transizione in cui la vecchia cornice scorre dalla vista e la nuova cornice scorre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> length  </span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica la durata (in secondi) dell'effetto di transizione <span class="codeph"> dissolvenza </span> o <span class="codeph"> diapositiva </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> spaziatura  </span> </span> </p> </td> 
   <td colname="col2"> <p>La spaziatura tra i fotogrammi adiacenti nella transizione <span class="codeph"> diapositiva </span> ha un intervallo compreso tra <span class="codeph"> 0 </span> e <span class="codeph"> 1 </span> ed è relativa alla larghezza del componente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

Nessuno.

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
