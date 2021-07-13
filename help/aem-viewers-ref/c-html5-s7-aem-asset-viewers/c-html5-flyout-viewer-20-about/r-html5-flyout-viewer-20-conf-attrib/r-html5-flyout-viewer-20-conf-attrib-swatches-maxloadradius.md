---
description: Swatches.maxloadradius
solution: Experience Manager
title: Swatches.maxloadradius
feature: Dynamic Media Classic,Visualizzatori,SDK/API,A comparsa
role: Developer,User
exl-id: b02f033d-be84-4cd0-b4bb-3ae9e424680c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 6%

---

# Swatches.maxloadradius{#swatches-maxloadradius}

` [Swatches.|<containerId>_swatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_4A27394B6B4347D69CAC5A59EE0FBC6F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> -1|0|<span class="varname"> precaricare</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica il comportamento di precaricamento del componente. Se è impostato su <span class="codeph"> -1</span>, tutti i campioni vengono caricati contemporaneamente quando il componente viene inizializzato o la risorsa viene modificata. Se è impostato su <span class="codeph"> 0</span> vengono caricati solo i campioni visibili. </p> <p><span class="codeph"> <span class="varname"> </span></span> precaricare definisce quante righe/colonne invisibili verranno precaricate intorno all’area visibile. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

`1`

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

`maxloadradius=-1`
