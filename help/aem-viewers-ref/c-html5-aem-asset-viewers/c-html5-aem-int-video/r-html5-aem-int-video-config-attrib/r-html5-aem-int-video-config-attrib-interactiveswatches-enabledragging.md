---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: InteractiveSwatches.enabledragging
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
exl-id: 91c5eb52-40d9-40f6-8687-e68cb40b634e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 5%

---

# InteractiveSwatches.enabledragging{#interactiveswatches-enabledragging}

Attributo di configurazione per Visualizzatore video interattivo.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Abilita o disabilita la possibilità per un utente di scorrere i campioni con il mouse o utilizzando movimenti touch. </p> </td> 
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
