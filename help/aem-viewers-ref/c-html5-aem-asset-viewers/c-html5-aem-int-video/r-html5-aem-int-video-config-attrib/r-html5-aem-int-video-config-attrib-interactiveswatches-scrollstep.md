---
description: Attributo di configurazione per Visualizzatore video interattivo.
seo-description: Attributo di configurazione per Visualizzatore video interattivo.
seo-title: InteractiveSwatches.scrollstep
solution: Experience Manager
title: InteractiveSwatches.scrollstep
uuid: 6f521aa4-9155-4f14-bc89-e7af24af25f0
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 4%

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

