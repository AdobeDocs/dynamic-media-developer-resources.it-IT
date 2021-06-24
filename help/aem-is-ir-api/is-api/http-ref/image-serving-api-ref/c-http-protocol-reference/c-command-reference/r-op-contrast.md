---
description: Regolare il contrasto. Regola il contrasto dell'immagine aumentando la luminosità dei pixel con una luminosità superiore al 50% e riducendo la luminosità dei pixel con una luminosità inferiore al 50%.
solution: Experience Manager
title: op_contrasto
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---

# op_contrasto{#op-contrast}

Regolare il contrasto. Regola il contrasto dell&#39;immagine aumentando la luminosità dei pixel con una luminosità superiore al 50% e riducendo la luminosità dei pixel con una luminosità inferiore al 50%.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Regolazione del contrasto in percentuale (-100...100 int). </p></td> 
 </tr> 
</table>

## Proprietà {#section-d319ed55057344eab0a3c93f720acdbf}

Livello, comando. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli di effetto.

## Predefinito {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, senza modifiche di contrasto. Le immagini o i livelli CMYK vengono convertiti in RGB prima dell’applicazione dell’operazione.

## Esempio {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Riduci il contrasto e la nitidezza di un livello di immagine di qualità superiore per adattarlo visivamente a una foto di sfondo di bassa qualità:

... `&op_blur=3&op_contrast=-12&`

Una versione futura potrebbe utilizzare la luminosità mediana dell&#39;immagine invece di una luminosità fissa del 50%.
