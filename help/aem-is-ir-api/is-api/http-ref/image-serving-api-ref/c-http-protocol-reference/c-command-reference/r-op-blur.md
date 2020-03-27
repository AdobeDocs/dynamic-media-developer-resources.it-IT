---
description: Sfoca immagine. Applica un filtro di sfocatura ai dati immagine.
seo-description: Sfoca immagine. Applica un filtro di sfocatura ai dati immagine.
seo-title: op_blur
solution: Experience Manager
title: op_blur
topic: Scene7 Image Serving - Image Rendering API
uuid: 8405bbb5-fe09-412e-9b52-0af2c01f48b9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_blur{#op-blur}

Sfoca immagine. Applica un filtro di sfocatura ai dati immagine.

`op_blur= *`radius`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>Raggio del filtro sfocatura in pixel (numero reale, da 0 a 100). </p></td> 
 </tr> 
</table>

*`radius`* è espressa in pixel rispetto all’immagine composita. Utilizzata anche per applicare la sfumatura agli effetti dei livelli.

## Proprietà {#section-92573fe2c07746a7bab93a81fc3d208d}

Livello, comando. Si applica al livello corrente o all’immagine composita, se `layer=comp`.

## Predefinito {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, per nessun effetto di sfocatura.

## Esempio {#section-1ebacde68388492eb108ae0fcd7424db}

Sfocate lo sfondo di un’immagine. Viene fatto riferimento a un&#39;immagine maschera separata da `catalog::MaskPath`. Notate che `layer=0`deve essere specificato esplicitamente, altrimenti `op_blur` verrà applicato all&#39;intera immagine composita.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
