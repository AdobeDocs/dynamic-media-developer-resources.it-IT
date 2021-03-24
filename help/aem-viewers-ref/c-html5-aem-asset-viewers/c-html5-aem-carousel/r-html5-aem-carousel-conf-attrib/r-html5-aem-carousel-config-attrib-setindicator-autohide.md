---
description: SetIndicator.autohide
solution: Experience Manager
title: SetIndicator.autohide
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 4%

---


# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`limite`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> limite</span>]</span> </p> </td> 
   <td colname="col2"> <p> Configura il comportamento di Nascondi automaticamente in base al numero di pagine e alle dimensioni del componente in fase di esecuzione. </p> <p> <span class="codeph"> 0</span> disattiva la funzione di nascondere automaticamente. </p> <p> <span class="codeph"> 1</span> abilita il mascheramento automatico. Il componente nasconde i punti se almeno una delle seguenti condizioni diventa vera: </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">la riga con punti diventa più larga della larghezza del componente in fase di esecuzione, oppure </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">il numero di pagine impostate per questo componente supera il limite configurato dal parametro <span class="codeph"><span class="varname"> limit</span></span> . </li> 
     </ul> </p> <p> L'impostazione di <span class="codeph"><span class="varname"> limit</span></span> a <span class="codeph"> -1</span> disattiva la seconda condizione di auto-hide. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1,10`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
