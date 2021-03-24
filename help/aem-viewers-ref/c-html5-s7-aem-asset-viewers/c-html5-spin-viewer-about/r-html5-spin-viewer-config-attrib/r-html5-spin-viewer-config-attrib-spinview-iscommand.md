---
description: SpinView.iscommand
solution: Experience Manager
title: SpinView.iscommand
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set 360 gradi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---


# SpinView.iscommand{#spinview-iscommand}

` [SpinView.|<containerId>_spinView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> Stringa di comando Image Server applicata all'immagine di rotazione. Se specificato nell'URL, tutte le occorrenze di <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> devono essere codificate per HTTP rispettivamente come <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>. </p> <p> <p>Nota:  I comandi di manipolazione del dimensionamento delle immagini non sono supportati. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

Nessuno.

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

Se specificato nell’URL del visualizzatore:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Se specificato nei dati di configurazione:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
