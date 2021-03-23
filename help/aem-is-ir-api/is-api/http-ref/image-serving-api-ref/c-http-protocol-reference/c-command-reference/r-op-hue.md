---
description: Regola la tonalità. Sposta la tonalità di ciascun pixel visibile del livello o dell'immagine composita in base alla quantità specificata.
seo-description: Regola la tonalità. Sposta la tonalità di ciascun pixel visibile del livello o dell'immagine composita in base alla quantità specificata.
seo-title: op_hue
solution: Experience Manager
title: op_hue
uuid: 23da539e-0192-4dc4-a19b-41aa94a82730
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 1%

---


# op_hue{#op-hue}

Regola la tonalità. Sposta la tonalità di ciascun pixel visibile del livello o dell&#39;immagine composita in base alla quantità specificata.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Regolazione del colore in gradi (-180..+180 int). </p></td> 
 </tr> 
</table>

Basato su una gamma di tonalità a 360 gradi.

## Proprietà {#section-55779644700b4c808a624cdf5a04447e}

Livello, comando. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli di effetto. Le immagini o i livelli CMYK vengono convertiti in RGB prima dell’applicazione dell’operazione.

## Predefinito {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, senza modifiche nella tonalità.
