---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura del doppio clic/tocco per attivare le azioni. Impostazione su <span class="codeph"> nessuno </span> disabilita il doppio clic o il doppio tocco. Se impostato su <span class="codeph"> zoom </span>, facendo clic sull'immagine che ruota in un passaggio di rotazione; CTRL+clic consente di eseguire un passaggio di rotazione. Impostazione su <span class="codeph"> reset </span> causa un singolo clic sull'immagine per ripristinare il livello di rotazione iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il reset se il fattore di rotazione corrente è pari o superiore al limite specificato, altrimenti viene applicato il spin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`reset` su computer desktop; `zoomReset` su dispositivi touch.

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
