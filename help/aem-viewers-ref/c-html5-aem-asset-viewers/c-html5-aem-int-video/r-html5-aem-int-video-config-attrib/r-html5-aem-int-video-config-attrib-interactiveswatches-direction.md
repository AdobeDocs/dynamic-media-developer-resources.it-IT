---
description: Attributo di configurazione per il visualizzatore video interattivo.
seo-description: Attributo di configurazione per il visualizzatore video interattivo.
seo-title: InteractiveSwatches.direction
solution: Experience Manager
title: InteractiveSwatches.direction
topic: Dynamic media
uuid: 08095ab5-f74b-4da6-8f8d-df377995455e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 4%

---


# InteractiveSwatches.direction{#interactiveswatches-direction}

Attributo di configurazione per il visualizzatore video interattivo.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> Specifica la modalità di riempimento dei campioni nella visualizzazione. </p> <p>Impostare su <span class="codeph"> sinistra </span> per impostare l'ordine di riempimento da sinistra a destra. </p> <p>Impostato su <span class="codeph"> destra </span> inverte l'ordine in modo che la vista sia riempita in una direzione da destra a sinistra e dall'alto verso il basso. </p> <p>Quando è impostata l'opzione <span class="codeph"> auto </span>, il componente applica la modalità corretta quando l'impostazione internazionale è impostata su " <span class="codeph"> ja </span>"; in caso contrario, viene utilizzato <span class="codeph"> a sinistra </span>. </p> </td> 
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

