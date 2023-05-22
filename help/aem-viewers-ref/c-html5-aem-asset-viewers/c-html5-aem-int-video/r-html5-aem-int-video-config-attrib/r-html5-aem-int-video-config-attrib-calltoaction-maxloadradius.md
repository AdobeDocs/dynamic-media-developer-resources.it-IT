---
title: CallToAction.maxloadradius
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 4%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Attributo di configurazione per Visualizzatore video interattivo.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il comportamento di precaricamento del componente. </p> <p>Se impostato su <span class="codeph"> -1</span> tutte le miniature vengono caricate contemporaneamente quando il componente viene inizializzato o la risorsa viene cambiata. </p> <p>Se impostato su <span class="codeph"> 0</span> vengono caricate solo le miniature visibili. </p> <p>Imposta su <span class="codeph"><span class="varname"> preloadnbr</span></span> per definire quante righe/colonne invisibili vengono precaricate attorno all'area visibile. </p> </td> 
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
