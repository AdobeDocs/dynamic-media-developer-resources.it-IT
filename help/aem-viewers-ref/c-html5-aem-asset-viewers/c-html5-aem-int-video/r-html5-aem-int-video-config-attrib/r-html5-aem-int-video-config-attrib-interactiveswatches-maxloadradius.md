---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: InteractiveSwatches.maxloadradius
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Developer,User
exl-id: 16c9c70a-352d-4a21-bb14-2f9e266a83e8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

Attributo di configurazione per Visualizzatore video interattivo.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> precaricare</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il comportamento di precaricamento del componente. </p> <p>Quando è impostato su <span class="codeph"> -1</span> tutti i campioni vengono caricati contemporaneamente quando il componente viene inizializzato o la risorsa viene modificata. </p> <p>Se è impostato su <span class="codeph"> 0</span> vengono caricati solo i campioni visibili. </p> <p>Impostare su <span class="codeph"><span class="varname"> preload</span></span> per definire quante righe/colonne invisibili vengono precaricate intorno all'area visibile. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
