---
description: Regola la tonalità. Sposta la tonalità di ciascun pixel visibile del livello o dell’immagine composita per la quantità specificata.
seo-description: Regola la tonalità. Sposta la tonalità di ciascun pixel visibile del livello o dell’immagine composita per la quantità specificata.
seo-title: op_hue
solution: Experience Manager
title: op_hue
topic: Scene7 Image Serving - Image Rendering API
uuid: 23da539e-0192-4dc4-a19b-41aa94a82730
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_hue{#op-hue}

Regola la tonalità. Sposta la tonalità di ciascun pixel visibile del livello o dell’immagine composita per la quantità specificata.

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Regolazione tonalità in gradi (-180...+180 punti). </p></td> 
 </tr> 
</table>

Basato su una gamma di tonalità di 360 gradi.

## Proprietà {#section-55779644700b4c808a624cdf5a04447e}

Livello, comando. Si applica al livello corrente o all’immagine composita, se `layer=comp`. Ignorato dai livelli degli effetti. Le immagini o i livelli CMYK vengono convertiti in RGB prima dell’applicazione dell’operazione.

## Predefinito {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`, per nessuna modifica nella tonalità.
