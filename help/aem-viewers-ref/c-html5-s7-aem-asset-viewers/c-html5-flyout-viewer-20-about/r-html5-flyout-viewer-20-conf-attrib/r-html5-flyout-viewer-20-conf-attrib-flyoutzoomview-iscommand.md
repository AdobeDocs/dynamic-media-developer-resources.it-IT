---
description: FlyoutZoomView.iscommand
solution: Experience Manager
title: FlyoutZoomView.iscommand
topic: Dynamic Media
uuid: 1e8dcafb-33ef-42ea-8636-b3b7de81dfbd
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---


# FlyoutZoomView.iscommand{#flyoutzoomview-iscommand}

` [FlyoutZoomView.|<containerId>_flyout.]iscommand= *`isCommand`*`

<table id="table_43A84C1044574A6FAB8CE67D71AAD5EC"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isCommand</span> </span> </p> </td> 
   <td colname="col2"> <p> </p> <p>Stringa del comando Image Server applicata all’immagine principale FlyoutZoomView e alla visualizzazione ingrandita. Se specificato nell'URL, assicurarsi di codificare tutte le occorrenze di <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> rispettivamente come <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>. </p> <p> <p>Nota:  I comandi di manipolazione del ridimensionamento delle immagini non sono supportati. </p> </p> </td> 
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

Quando specificato nei dati di configurazione:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
