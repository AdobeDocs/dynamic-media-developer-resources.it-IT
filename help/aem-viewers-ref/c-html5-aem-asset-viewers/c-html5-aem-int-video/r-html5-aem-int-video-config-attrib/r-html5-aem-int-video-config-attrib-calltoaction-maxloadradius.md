---
description: Attributo di configurazione per il visualizzatore video interattivo.
seo-description: Attributo di configurazione per il visualizzatore video interattivo.
seo-title: CallToAction.maxloadradius
solution: Experience Manager
title: CallToAction.maxloadradius
topic: Dynamic Media
uuid: ec5a4b0d-1dae-456f-a9da-91541cfba1a7
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---


# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Attributo di configurazione per il visualizzatore video interattivo.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> precaricatore</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il comportamento di precaricamento del componente. </p> <p>Se è impostata su <span class="codeph"> -1</span>, tutte le miniature vengono caricate contemporaneamente quando il componente viene inizializzato o la risorsa viene modificata. </p> <p>Se impostato su <span class="codeph"> 0</span> vengono caricate solo le miniature visibili. </p> <p>Impostare su <span class="codeph"><span class="varname"> precaricatore</span></span> per definire quante righe/colonne invisibili vengono precaricate intorno all'area visibile. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`-1`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```

