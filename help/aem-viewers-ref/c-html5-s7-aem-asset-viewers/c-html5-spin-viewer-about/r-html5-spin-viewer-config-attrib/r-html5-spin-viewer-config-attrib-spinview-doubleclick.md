---
description: SpinView.doubleclick
solution: Experience Manager
title: SpinView.doubleclick
uuid: c1eef3d1-471e-41ef-b899-008d45b616d0
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set 360 gradi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---


# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset  </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura del doppio clic/tocco per attivare le azioni. Se si imposta su <span class="codeph"> none </span>, viene disattivato il doppio clic o il doppio tocco. Se è impostato su <span class="codeph"> zoom </span> facendo clic sull'immagine si verifica un giro in un unico passaggio; CTRL+clic consente di eseguire un passaggio di rotazione. Impostando su <span class="codeph"> reset </span> si reimposta un singolo clic sull'immagine per ripristinare la rotazione al livello iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il reset se il fattore di rotazione corrente è pari o superiore al limite specificato, altrimenti viene applicato il spin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`reset` su computer desktop;  `zoomReset` su dispositivi touch.

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
