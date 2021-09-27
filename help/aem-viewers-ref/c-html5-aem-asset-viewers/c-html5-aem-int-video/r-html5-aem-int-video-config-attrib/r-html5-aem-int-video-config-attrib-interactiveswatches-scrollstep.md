---
title: InteractiveSwatches.scrollstep
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 15bf7af8-428b-4c1c-b7ad-004563347d7c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 6%

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
