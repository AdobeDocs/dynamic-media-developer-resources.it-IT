---
title: CallToAction.textpos
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f2356eb1-2f71-49b6-bb40-6cd332e6785b
TQID: 'https://experienceleague.adobe.com/9B1zIGEH3j96hpJXcQcZfgDqxR6oHuBt611qL2O4oq4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 74
ht-degree: 4%

---

# CallToAction.textpos{#calltoaction-textpos}

Attributo di configurazione per Visualizzatore video interattivo.

`[CallToAction.|<containerId>_callToAction.]textpos=bottom|top|left|right|none|tooltip`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> in basso|in alto|a sinistra|a destra|nessuno|descrizione comando</span> </p> </td> 
   <td colname="col2"> <p> Specifica dove viene disegnata l'etichetta rispetto all'immagine miniatura. In altre parole, l’etichetta viene centrata nella posizione specificata relativa alla miniatura. </p> <p>Quando si specifica la descrizione <span class="codeph"></span>, il testo dell'etichetta viene visualizzato come descrizione mobile sopra l'immagine di anteprima. </p> <p>Impostare su <span class="codeph"> none</span> per disattivare l'etichetta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-1e637b22e8a44d759d588e47576891e6}

Facoltativo.

## Predefinito {#section-71fb773f814649b2885aefee68073641}

`bottom`

## Esempio {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
textpos=top
```
