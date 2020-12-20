---
description: 'null'
seo-description: 'null'
seo-title: SetIndicator.autohide
solution: Experience Manager
title: SetIndicator.autohide
topic: Dynamic media
uuid: eb93ad7a-6176-47ed-92c6-2eb1afcac0eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 5%

---


# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`limit`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> limite</span>]</span> </p> </td> 
   <td colname="col2"> <p> Configura il comportamento di disattivazione automatica in base al numero di pagine e alle dimensioni del componente in fase di esecuzione. </p> <p> <span class="codeph"> 0</span> disattiva l'opzione Nascondi automatico. </p> <p> <span class="codeph"> 1 </span> abilita la funzione di disattivazione automatica. Il componente nasconde i punti se almeno una delle seguenti condizioni diventa true: </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">la riga con punti diventa più larga della larghezza del componente in fase di esecuzione, oppure </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">il numero di pagine impostato per questo componente supera il limite configurato dal parametro <span class="codeph"><span class="varname"> limit</span></span>. </li> 
     </ul> </p> <p> Se si imposta <span class="codeph"><span class="varname"> limit</span></span> su <span class="codeph"> -1</span>, viene disattivata la seconda condizione di disattivazione automatica. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`1,10`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
