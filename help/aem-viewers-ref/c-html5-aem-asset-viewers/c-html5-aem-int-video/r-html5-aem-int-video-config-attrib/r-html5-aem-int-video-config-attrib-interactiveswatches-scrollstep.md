---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: InteractiveSwatches.scrollstep
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
exl-id: 15bf7af8-428b-4c1c-b7ad-004563347d7c
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---

# InteractiveSwatches.scrollstep{#interactiveswatches-scrollstep}

Attributo di configurazione per Visualizzatore video interattivo.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]scrollstep= *`step`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> step</span></span> </p> </td> 
   <td colname="col2"> <p>Specifica il numero di campioni da scorrere per ogni tocco del pulsante di scorrimento corrispondente. </p> <p>Se il valore specificato è maggiore del numero di campioni interattivi visibili, ogni tocco scorre solo in base al numero di campioni visibili per evitare l’omissione di un campione. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`3`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
scrollstep=1
```
