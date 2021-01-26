---
description: Applica i flag. Specifica ulteriori opzioni di rendering.
seo-description: Applica i flag. Specifica ulteriori opzioni di rendering.
seo-title: flag
solution: Experience Manager
title: flag
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 43ed24fe-461e-4973-aa44-8fba66668e6f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 2%

---


# flags{#flags}

Applica i flag. Specifica ulteriori opzioni di rendering.

`flags= *`val`*`

<table id="simpletable_00B21BD9E47E4D2FB0042CB507431916"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Valore contrassegno. </p></td> 
 </tr> 
</table>

Attualmente utilizzato solo per i materiali di armadio.

`flags=0` (impostazione predefinita) esegue il rendering degli armadi superiori con porte solide.

`flags=1` riproduce gli armadi superiori con porte in vetro (se la vignettatura è stata creata con porte in vetro).

## Proprietà {#section-a2b00d7bb15e449ea85178acb92d8285}

Attributo materiale. Ignorato se non è presente un materiale mobile o se l&#39;oggetto cabinet di destinazione non consente porte in vetro.

## Predefinito {#section-4c134b02a1da4ffb9841233f98f6e97c}

`flags=0` senza porte in vetro.
