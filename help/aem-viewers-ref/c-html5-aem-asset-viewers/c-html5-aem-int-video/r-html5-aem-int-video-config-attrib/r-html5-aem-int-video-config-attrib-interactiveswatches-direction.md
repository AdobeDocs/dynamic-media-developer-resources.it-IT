---
description: Attributo di configurazione per Visualizzatore video interattivo.
seo-description: Attributo di configurazione per Visualizzatore video interattivo.
seo-title: InteractiveSwatches.direction
solution: Experience Manager
title: InteractiveSwatches.direction
uuid: 08095ab5-f74b-4da6-8f8d-df377995455e
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---


# InteractiveSwatches.direction{#interactiveswatches-direction}

Attributo di configurazione per Visualizzatore video interattivo.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|sinistra|destra  </span> </p> </td> 
   <td colname="col2"> <p> Specifica il modo in cui i campioni vengono riempiti nella visualizzazione. </p> <p>Impostare su <span class="codeph"> sinistra </span> per impostare l'ordine di riempimento da sinistra a destra. </p> <p>Impostato su <span class="codeph"> destra </span> inverte l'ordine in modo che la visualizzazione sia riempita in una direzione da destra a sinistra e dall'alto verso il basso. </p> <p>Quando è impostato <span class="codeph"> auto </span>, il componente applica la modalità corretta quando le impostazioni internazionali sono impostate su " <span class="codeph"> ja </span>"; in caso contrario, viene utilizzato <span class="codeph"> sinistro </span>. </p> </td> 
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

