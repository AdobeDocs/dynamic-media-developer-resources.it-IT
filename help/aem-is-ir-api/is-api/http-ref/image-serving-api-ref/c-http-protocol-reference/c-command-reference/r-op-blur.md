---
description: Sfoca immagine. Applica un filtro di sfocatura ai dati immagine.
solution: Experience Manager
title: op_blur
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# op_blur{#op-blur}

Sfoca immagine. Applica un filtro di sfocatura ai dati immagine.

`op_blur= *`raggio`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> raggio</span> </p> </td> 
  <td class="stentry"> <p>Raggio filtro sfocatura in pixel (reale 0..100). </p></td> 
 </tr> 
</table>

*`radius`* è in pixel rispetto all&#39;immagine composita. Utilizzato anche per sfumare gli effetti di livello.

## Proprietà {#section-92573fe2c07746a7bab93a81fc3d208d}

Comando Livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`.

## Predefinito {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, senza effetto sfocatura.

## Esempio {#section-1ebacde68388492eb108ae0fcd7424db}

Sfoca lo sfondo di un&#39;immagine. Viene fatto riferimento a un&#39;immagine maschera separata da `catalog::MaskPath`. Tieni presente che `layer=0`deve essere specificato in modo esplicito, altrimenti `op_blur` all&#39;intera immagine composita.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
