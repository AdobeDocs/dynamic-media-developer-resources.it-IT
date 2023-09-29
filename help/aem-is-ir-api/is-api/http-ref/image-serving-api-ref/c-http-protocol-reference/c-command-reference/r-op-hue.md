---
title: op_hue
description: Regola la tonalità dell'immagine. Sposta la tonalità di ciascun pixel visibile del livello o dell'immagine composita della quantità specificata.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---

# op_hue{#op-hue}

Regola la tonalità dell&#39;immagine. Sposta la tonalità di ciascun pixel visibile del livello o dell&#39;immagine composita della quantità specificata.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Regolazione tonalità in gradi (-180...+180 int). </p></td> 
 </tr> 
</table>

Basato su una gamma di tonalità a 360 gradi.

## Proprietà {#section-55779644700b4c808a624cdf5a04447e}

Comando Livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli degli effetti. Le immagini o i livelli CMYK vengono convertiti in RGB prima dell&#39;applicazione dell&#39;operazione.

## Predefinito {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, senza alcuna modifica della tonalità.
