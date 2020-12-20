---
description: 'null'
seo-description: 'null'
seo-title: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
topic: Dynamic media
uuid: c1eef3d1-471e-41ef-b899-008d45b616d0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura di azioni con doppio clic o tocco per le azioni di rotazione. Se si imposta su <span class="codeph"> none </span>, viene disattivato il doppio clic o il tocco. Se impostato su <span class="codeph"> zoom </span> facendo clic sulle rotazioni dell'immagine in un unico passaggio di rotazione, CTRL+clic consente di ruotare un passaggio di rotazione. Se si imposta <span class="codeph"> reset </span>, l'immagine viene reimpostata con un solo clic per ripristinare il livello iniziale di rotazione. Per <span class="codeph"> zoomReset </span>, reimposta se il fattore di rotazione corrente è uguale o superiore al limite specificato, altrimenti viene applicato il spin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`reset` su computer desktop;  `zoomReset` su dispositivi touch.

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
