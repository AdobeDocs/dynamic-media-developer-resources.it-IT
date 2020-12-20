---
description: Regolare il contrasto. Regola il contrasto dell’immagine aumentando la luminosità dei pixel con una luminosità superiore al 50% e riducendo la luminosità dei pixel con una luminosità inferiore al 50%.
seo-description: Regolare il contrasto. Regola il contrasto dell’immagine aumentando la luminosità dei pixel con una luminosità superiore al 50% e riducendo la luminosità dei pixel con una luminosità inferiore al 50%.
seo-title: op_contrasto
solution: Experience Manager
title: op_contrasto
topic: Scene7 Image Serving - Image Rendering API
uuid: d17b0b49-792b-41ce-a154-5e7635c9ab43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 1%

---


# op_contrasto{#op-contrast}

Regolare il contrasto. Regola il contrasto dell’immagine aumentando la luminosità dei pixel con una luminosità superiore al 50% e riducendo la luminosità dei pixel con una luminosità inferiore al 50%.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Regolazione del contrasto in percentuale (-100...100 int). </p></td> 
 </tr> 
</table>

## Proprietà {#section-d319ed55057344eab0a3c93f720acdbf}

Livello, comando. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli degli effetti.

## Predefinito {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, per nessun cambiamento di contrasto. Le immagini o i livelli CMYK vengono convertiti in RGB prima dell’applicazione dell’operazione.

## Esempio {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Per ridurre il contrasto e la nitidezza di un livello di immagine di qualità superiore e ottenere una corrispondenza visiva con una foto di sfondo di bassa qualità:

... `&op_blur=3&op_contrast=-12&`

In una versione futura è possibile utilizzare la luminosità media dell’immagine anziché una luminosità fissa del 50%.
