---
title: op_blur
description: Sfoca immagine. Applica un filtro di sfocatura ai dati immagine.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
TQID: 'https://experienceleague.adobe.com/e7GXc5NYZC2Flk0Uf71iw-hi-gPdQk-XldMpPH-DwqM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 2%

---

# op_blur{#op-blur}

Sfoca immagine. Applica un filtro di sfocatura ai dati immagine.

`op_blur= *`raggio`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Raggio <span class="varname"></span> </p> </td> 
  <td class="stentry"> <p>Raggio filtro sfocatura in pixel (reale 0..100). </p></td> 
 </tr> 
</table>

*`radius`* è in pixel rispetto all&#39;immagine composita. Utilizzato anche per sfumare gli effetti di livello.

## Proprietà {#section-92573fe2c07746a7bab93a81fc3d208d}

Comando Livello. Si applica al livello corrente o all&#39;immagine composita se `layer=comp`.

## Predefinito {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`, senza effetto sfocatura.

## Esempio {#section-1ebacde68388492eb108ae0fcd7424db}

Sfoca lo sfondo di un&#39;immagine. `catalog::MaskPath` fa riferimento a un&#39;immagine di maschera separata. `layer=0` deve essere specificato in modo esplicito, altrimenti `op_blur` verrà applicato all&#39;intera immagine composita.

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
