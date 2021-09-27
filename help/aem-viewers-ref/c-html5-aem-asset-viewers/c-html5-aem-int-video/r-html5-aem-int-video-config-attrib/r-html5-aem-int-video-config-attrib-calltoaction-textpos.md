---
title: CallToAction.textpos
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f2356eb1-2f71-49b6-bb40-6cd332e6785b
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 5%

---

# CallToAction.textpos{#calltoaction-textpos}

Attributo di configurazione per Visualizzatore video interattivo.

`[CallToAction.|<containerId>_callToAction.]textpos=bottom|top|left|right|none|tooltip`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> in basso|in alto|a sinistra|a destra|nessuno|descrizione comandi</span> </p> </td> 
   <td colname="col2"> <p> Specifica dove viene disegnata l’etichetta rispetto all’immagine in miniatura. In altre parole, l’etichetta viene centrata nella posizione specificata relativa alla miniatura. </p> <p>Quando si specifica <span class="codeph"> tooltip</span>, il testo dell'etichetta viene visualizzato come una descrizione mobile sopra l'immagine miniatura. </p> <p>Impostare su <span class="codeph"> none</span> per disattivare l'etichetta. </p> </td> 
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
