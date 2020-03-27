---
description: 'null'
seo-description: 'null'
seo-title: SpinView.iscommand
solution: Experience Manager
title: SpinView.iscommand
topic: Dynamic media
uuid: 791164a1-93fa-411f-9fb8-f78efb96f16b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.iscommand{#spinview-iscommand}

` [SpinView.|<containerId>_spinView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> Stringa di comando Image Server applicata all’immagine con rotazione. Se specificate nell’URL, tutte le occorrenze di <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> devono essere codificate rispettivamente in HTTP come <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>. </p> <p> <p>Nota:  I comandi di manipolazione del ridimensionamento delle immagini non sono supportati. </p> </p> </td> 
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
