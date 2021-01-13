---
description: Swatches.iscommand
solution: Experience Manager
title: Swatches.iscommand
topic: Dynamic media
uuid: 6fa79ce2-5191-4282-acee-5c6caad24fba
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---


# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Stringa di comando Image Server applicata a tutti i campioni. Se specificato nell'URL, assicurarsi di codificare tutte le occorrenze di <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> rispettivamente come <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>. </p> <p> <p>Nota:  I comandi di manipolazione del ridimensionamento delle immagini non sono supportati. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

Nessuno.

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

Se specificato nell’URL del visualizzatore.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Se specificato nei dati di configurazione.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
