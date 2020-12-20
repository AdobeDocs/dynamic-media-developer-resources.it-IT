---
description: Regolare il bilanciamento del colore. Regola separatamente il valore di ciascun componente di colore RGB.
seo-description: Regolare il bilanciamento del colore. Regola separatamente il valore di ciascun componente di colore RGB.
seo-title: op_colorbalance
solution: Experience Manager
title: op_colorbalance
topic: Scene7 Image Serving - Image Rendering API
uuid: 177aa6e3-1b32-4254-85f1-d7fe14116e3c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---


# op_colorbalance{#op-colorbalance}

Regolare il bilanciamento del colore. Regola separatamente il valore di ciascun componente di colore RGB.

`op_colorbalance= *``*, *``*, *`redAdjgreenAdjblueAdj`*`

<table id="simpletable_BBDAA6FE9A0E48E3BD8304BDED776713"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> redAdj</span> </p></td> 
  <td class="stentry"> <p>Regolazione componente rosso (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> greenAdj</span> </p></td> 
  <td class="stentry"> <p>Regolazione del componente verde (-100...+100 int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> blueAdj</span> </p></td> 
  <td class="stentry"> <p>Regolazione del componente blu (-100...+100 int). </p></td> 
 </tr> 
</table>

I dati delle immagini in ingresso Grigio e CMYK vengono convertiti in RGB utilizzando una conversione ingenua che non è precisa quando è abilitata la gestione del colore.

## Proprietà {#section-dff9c934f7c1442bbd02379b688d82e2}

Livello, comando. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli degli effetti. Le immagini e i livelli CMYK vengono convertiti in RGB prima dell’applicazione dell’operazione.

## Predefinito {#section-08d84ef715964f7daea86f5ef237d199}

`op_colorbalance=0,0,0` per non modificare i colori.

## Esempio {#section-7e97fa36e01d4af8ab03fc9d493da1a1}

Spinge il bilanciamento del colore verso il rosso:

... `&op_colorBalance=100,0,0&`...
