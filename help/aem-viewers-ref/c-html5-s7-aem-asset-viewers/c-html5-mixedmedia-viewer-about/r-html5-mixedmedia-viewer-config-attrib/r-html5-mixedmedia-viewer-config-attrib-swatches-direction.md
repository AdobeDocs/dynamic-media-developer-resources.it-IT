---
title: Swatches.direction
description: Swatches.direction
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: bd01ff03-fea7-42ad-aa99-72273f55bda0
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
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

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`direction=right`
