---
description: Attributo di configurazione per Visualizzatore video interattivo.
seo-description: Attributo di configurazione per Visualizzatore video interattivo.
seo-title: CallToAction.enabledragging
solution: Experience Manager
title: CallToAction.enabledragging
uuid: efb272b5-e30e-44d5-9dec-0529b1074ed2
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 4%

---


# CallToAction.enabledragging{#calltoaction-enabledragging}

Attributo di configurazione per Visualizzatore video interattivo.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Abilita o disabilita lo scorrimento delle miniature con il mouse o tramite movimenti touch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td colname="col2"> <p> Si trova nell'intervallo <span class="codeph"> 0-1 </span> ed è un valore percentuale del movimento nella direzione sbagliata della velocità effettiva. </p> <p>Se impostato su <span class="codeph"> 1 </span> si sposta con il mouse. </p> <p>Se impostato su <span class="codeph"> 0 </span> non consente di spostarsi nella direzione sbagliata. </p> </td> 
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

