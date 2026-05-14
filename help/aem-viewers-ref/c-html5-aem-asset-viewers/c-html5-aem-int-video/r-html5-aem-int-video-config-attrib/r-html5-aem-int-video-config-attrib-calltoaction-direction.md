---
title: CallToAction.direction
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
TQID: 'https://experienceleague.adobe.com/YehjMoK88ylklqHA9ZpjPgW8xoMwhLQqR-2e73ayWRM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 82
ht-degree: 3%

---

# CallToAction.direction{#calltoaction-direction}

Attributo di configurazione per Visualizzatore video interattivo.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|sinistra|destra </span> </p> </td> 
   <td colname="col2"> <p> Specifica il modo in cui le miniature vengono visualizzate. </p> <p>Impostare su <span class="codeph"> a sinistra di </span> per impostare l'ordine di riempimento da sinistra a destra. </p> <p>Impostato su <span class="codeph"> a destra </span> inverte l'ordine in modo che la visualizzazione venga riempita da destra a sinistra e dall'alto al basso. </p> <p>Impostare su <span class="codeph"> auto </span> per applicare la modalità destra al componente quando le impostazioni locali sono impostate su <span class="codeph"> "ja" </span>; in caso contrario, viene utilizzato <span class="codeph"> left </span>. </p> </td> 
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
