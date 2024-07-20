---
title: InteractiveSwatches.direction
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 4%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

Attributo di configurazione per Visualizzatore video interattivo.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|sinistra|destra </span> </p> </td> 
   <td colname="col2"> <p> Specifica il modo in cui i campioni vengono visualizzati. </p> <p>Impostare su <span class="codeph"> a sinistra di </span> per impostare l'ordine di riempimento da sinistra a destra. </p> <p>Impostato su <span class="codeph"> a destra </span> inverte l'ordine in modo che la visualizzazione venga riempita da destra a sinistra e dall'alto al basso. </p> <p>Quando è impostato <span class="codeph"> auto </span>, il componente applica la modalità destra quando le impostazioni locali sono impostate su " <span class="codeph"> ja </span>"; in caso contrario, viene utilizzato <span class="codeph"> left </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`auto`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```
