---
title: SetIndicator.autohide
description: SetIndicator.autohide
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 3%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`limit`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[<span class="varname"> limit</span>]</span> </p> </td> 
   <td colname="col2"> <p> Configura il comportamento Nascondi automatico in base al numero di pagine e alle dimensioni del componente in fase di esecuzione. </p> <p> <span class="codeph"> 0</span> disattiva la funzione Nascondi automaticamente. </p> <p> <span class="codeph"> 1</span> abilita nascondi automatico. Il componente nasconde i punti se almeno una delle seguenti condizioni diventa vera: </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">la riga con punti diventa più lunga della larghezza del componente di runtime, oppure </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">il numero di pagine impostato per questo componente supera il limite configurato da <span class="codeph"><span class="varname"> limit</span></span> parametro. </li> 
     </ul> </p> <p> Impostazione <span class="codeph"><span class="varname"> limit</span></span> a <span class="codeph"> -1</span> disabilita la seconda condizione di nascondi automatico. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1,10`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
