---
description: Regola tonalità. Sposta la tonalità di ciascun pixel visibile del livello o dell'immagine composita della quantità specificata.
solution: Experience Manager
title: op_hue
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# op_hue{#op-hue}

Regola tonalità. Sposta la tonalità di ciascun pixel visibile del livello o dell&#39;immagine composita della quantità specificata.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Regolazione tonalità in gradi (-180...+180 int). </p></td> 
 </tr> 
</table>

Basato su una gamma di tonalità di 360 gradi.

## Proprietà {#section-55779644700b4c808a624cdf5a04447e}

Comando Livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli degli effetti. Le immagini o i livelli CMYK vengono convertiti in RGB prima dell&#39;applicazione dell&#39;operazione.

## Predefinito {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, senza alcuna modifica della tonalità.
