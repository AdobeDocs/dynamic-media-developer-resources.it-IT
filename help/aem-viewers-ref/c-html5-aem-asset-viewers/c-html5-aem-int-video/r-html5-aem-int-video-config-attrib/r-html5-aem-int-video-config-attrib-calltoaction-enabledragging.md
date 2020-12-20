---
description: Attributo di configurazione per il visualizzatore video interattivo.
seo-description: Attributo di configurazione per il visualizzatore video interattivo.
seo-title: CallToAction.enabledragging
solution: Experience Manager
title: CallToAction.enabledragging
topic: Dynamic media
uuid: efb272b5-e30e-44d5-9dec-0529b1074ed2
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 5%

---


# CallToAction.enabledragging{#calltoaction-enabledragging}

Attributo di configurazione per il visualizzatore video interattivo.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Abilita o disabilita la possibilità per un utente di scorrere le miniature con il mouse o mediante gesti touch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td colname="col2"> <p> Si trova nell'intervallo <span class="codeph"> 0-1 </span> ed è un valore percentuale per il movimento nella direzione sbagliata della velocità effettiva. </p> <p>Se impostato su <span class="codeph"> 1 </span> si sposta con il mouse. </p> <p>Se impostato su <span class="codeph"> 0 </span> non consente di spostarsi nella direzione sbagliata. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```

