---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: CallToAction.direction
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Developer,Business Practitioner
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# CallToAction.direction{#calltoaction-direction}

Attributo di configurazione per Visualizzatore video interattivo.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|sinistra|destra  </span> </p> </td> 
   <td colname="col2"> <p> Specifica il modo in cui le miniature vengono compilate nella visualizzazione. </p> <p>Impostare su <span class="codeph"> sinistra </span> per impostare l'ordine di riempimento da sinistra a destra. </p> <p>Impostato su <span class="codeph"> destra </span> inverte l'ordine in modo che la visualizzazione sia riempita in una direzione da destra a sinistra e dall'alto verso il basso. </p> <p>Impostare su <span class="codeph"> auto </span> affinché il componente applichi la modalità a destra quando le impostazioni internazionali sono impostate su <span class="codeph"> "ja" </span>; in caso contrario, viene utilizzato <span class="codeph"> sinistro </span>. </p> </td> 
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
