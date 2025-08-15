---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`durata`*[, *`spaziatura`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nessuna|dissolvenza|diapositiva </span> </p> </td> 
   <td colname="col2"> <p>Specifica il tipo di effetto applicato al cambio di fotogramma. L'attributo <span class="codeph"> none </span> non rappresenta alcuna transizione; la modifica del frame avviene immediatamente. L'attributo <span class="codeph"> dissolvenza </span> indica una transizione di dissolvenza incrociata tra i fotogrammi vecchi e nuovi. L'attributo <span class="codeph"> diapositiva </span> attiva la transizione in cui il vecchio frame scorre fuori dalla visualizzazione e il nuovo frame scorre all'interno. </p> </td> 
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

`frametransition=fade,1`
