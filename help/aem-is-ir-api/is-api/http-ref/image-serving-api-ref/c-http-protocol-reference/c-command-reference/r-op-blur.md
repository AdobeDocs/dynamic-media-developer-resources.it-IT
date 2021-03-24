---
description: Sfoca immagine. Applica un filtro di sfocatura ai dati dell'immagine.
solution: Experience Manager
title: op_blur
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---


# op_blur{#op-blur}

Sfoca immagine. Applica un filtro di sfocatura ai dati dell&#39;immagine.

`op_blur= *`raggio`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> raggio</span> </p> </td> 
  <td class="stentry"> <p>Raggio del filtro sfocatura in pixel (reale 0.100). </p></td> 
 </tr> 
</table>

*`radius`* è in pixel rispetto all&#39;immagine composita. Utilizzato anche per piumare gli effetti di livello.

## Proprietà {#section-92573fe2c07746a7bab93a81fc3d208d}

Livello, comando. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`.

## Predefinito {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, senza effetto sfocatura.

## Esempio {#section-1ebacde68388492eb108ae0fcd7424db}

Sfoca lo sfondo di un&#39;immagine. A un&#39;immagine maschera separata viene fatto riferimento da `catalog::MaskPath`. Si noti che `layer=0`deve essere specificato esplicitamente, altrimenti `op_blur` verrebbe applicato all&#39;intera immagine composita.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
