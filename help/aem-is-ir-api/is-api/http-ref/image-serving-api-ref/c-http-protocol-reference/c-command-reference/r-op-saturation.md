---
description: Regolare la saturazione. Modifica la saturazione di ogni pixel visibile del livello o dell'immagine composita.
solution: Experience Manager
title: op_saturation
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# op_saturation{#op-saturation}

Regolare la saturazione. Modifica la saturazione di ogni pixel visibile del livello o dell&#39;immagine composita.

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Regolazione della saturazione (-100...+100 int). </p></td> 
 </tr> 
</table>

`op_saturation=-100` desatura completamente l&#39;immagine.

## Proprietà {#section-9a3cc9ff060049449554dfa69d92fd53}

Livello, comando. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`. Ignorato dai livelli di effetto.

## Predefinito {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, senza alcun cambiamento nella saturazione. Le immagini o i livelli CMYK vengono convertiti in RGB prima dell’applicazione dell’operazione.

## Esempio {#section-033b272f1b7e4efeb94e841fd8095357}

Manipolare una fotografia a colori per ottenere un aspetto &quot;high key&quot;:

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
