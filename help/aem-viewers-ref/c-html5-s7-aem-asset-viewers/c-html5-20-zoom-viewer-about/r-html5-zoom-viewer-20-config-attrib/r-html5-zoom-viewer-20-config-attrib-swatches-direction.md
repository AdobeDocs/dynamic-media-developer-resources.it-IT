---
title: Swatches.direction
description: Swatches.direction
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 906541bc-46dd-4a7c-8ee9-eb45ec3bd340
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# Swatches.direction{#swatches-direction}

`[Swatches.|<containerId>_swatches.]direction=auto|left|right`

<table id="table_B4B930A32C0742F4932BF071B9EEA9F4"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> auto|sinistra|destra </span> </p> </td> 
   <td> <p> Specifica il modo in cui i campioni vengono riempiti nella visualizzazione. </p> <p> <span class="codeph"> sinistra </span> imposta l'ordine di riempimento da sinistra a destra; </p> <p> <span class="codeph"> right </span> inverte l’ordine in modo che la visualizzazione venga riempita da destra a sinistra e dall’alto verso il basso. </p> <p>Quando <span class="codeph"> auto </span> è impostato, il componente si applica <span class="codeph"> right </span> quando le impostazioni internazionali sono impostate su <span class="codeph"> ja </span>; in caso contrario, viene utilizzato sinistra. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`auto`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

`direction=right`
