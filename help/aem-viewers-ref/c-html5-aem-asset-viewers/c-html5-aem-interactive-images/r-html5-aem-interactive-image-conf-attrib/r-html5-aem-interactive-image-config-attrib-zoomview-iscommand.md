---
title: ZoomView.iscommand
description: Stringa di comando Image Server applicata all'immagine di zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 1c24973e-1daf-4d9d-b97c-fb6a18f506ed
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 6%

---

# ZoomView.iscommand{#zoomview-iscommand}

Stringa di comando Image Server applicata all&#39;immagine di zoom.

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> Se specificato nell’URL, tutte le occorrenze di <span class="codeph"> E</span> e <span class="codeph"> =</span> deve essere codificato HTTP come <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>, rispettivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

Nessuno.

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

Se specificato nell’URL del visualizzatore:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Se specificato nei dati di configurazione:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
