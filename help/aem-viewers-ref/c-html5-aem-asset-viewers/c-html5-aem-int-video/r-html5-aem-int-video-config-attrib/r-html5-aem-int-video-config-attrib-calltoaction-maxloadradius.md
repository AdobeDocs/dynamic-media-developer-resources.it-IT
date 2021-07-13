---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: CallToAction.maxloadradius
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Attributo di configurazione per Visualizzatore video interattivo.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> precaricare</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il comportamento di precaricamento del componente. </p> <p>Se è impostato su <span class="codeph"> -1</span>, tutte le miniature vengono caricate simultaneamente quando il componente viene inizializzato o la risorsa viene modificata. </p> <p>Se impostato su <span class="codeph"> 0</span> vengono caricate solo le miniature visibili. </p> <p>Impostare su <span class="codeph"><span class="varname"> preload</span></span> per definire quante righe/colonne invisibili vengono precaricate intorno all'area visibile. </p> </td> 
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
