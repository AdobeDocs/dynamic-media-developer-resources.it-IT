---
title: Swatches.iscommand
description: Swatches.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: ed587082-3306-4914-916f-db37a823e199
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 6%

---

# Swatches.iscommand{#swatches-iscommand}

` [Swatches.|<containerId>_swatches.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> Stringa di comando Image Server applicata a tutti i campioni. Se è specificato nell’URL, accertati di codificare HTTP tutte le occorrenze di <span class="codeph"> E</span> e <span class="codeph"> =</span> as <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>, rispettivamente. </p> <p> <p>Nota: i comandi di manipolazione del ridimensionamento delle immagini non sono supportati. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facoltativo.

## Predefinito {#section-a08032f0fcf041c09e63c0238a339fc9}

Nessuno.

## Esempio {#section-0338be21edd04ff1a3bed5c8319b61a4}

Se specificato nell’URL del visualizzatore:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Se specificato nei dati di configurazione:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
