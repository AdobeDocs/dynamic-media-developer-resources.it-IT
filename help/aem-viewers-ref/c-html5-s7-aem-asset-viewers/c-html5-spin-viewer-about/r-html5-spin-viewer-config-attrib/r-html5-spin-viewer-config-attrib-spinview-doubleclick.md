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
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> Configura la mappatura delle azioni di doppio clic/tocco per eseguire la rotazione. L'impostazione su <span class="codeph"> none </span> disabilita la rotazione tramite doppio clic/tocco. Se è impostato su <span class="codeph">, zoom </span>, facendo clic sull'immagine viene eseguito un passaggio di rotazione; premendo CTRL l'immagine viene eseguito un passaggio di rotazione. L'impostazione su <span class="codeph"> reimposta </span> fa sì che un singolo clic sull'immagine ripristini il livello di rotazione iniziale. Per <span class="codeph"> zoomReset </span>, viene applicato il ripristino se il fattore di rotazione corrente è pari o superiore al limite specificato, altrimenti viene applicato lo spin. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-924163cb2f6542499f49894becef7fb5}

Facoltativo.

## Predefinito {#section-7a2128fd488941948aff18421f533ccf}

`reset` nei computer desktop; `zoomReset` nei dispositivi touch.

## Esempio {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
