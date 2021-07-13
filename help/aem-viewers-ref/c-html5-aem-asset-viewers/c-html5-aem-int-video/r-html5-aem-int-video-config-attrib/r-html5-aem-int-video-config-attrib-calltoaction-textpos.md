---
description: Attributo di configurazione per Visualizzatore video interattivo.
solution: Experience Manager
title: CallToAction.textpos
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Developer,User
exl-id: f2356eb1-2f71-49b6-bb40-6cd332e6785b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

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
