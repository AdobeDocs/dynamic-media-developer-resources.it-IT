---
title: Dimensione
description: Dimensione decalcomania. Larghezza, altezza e spessore di un oggetto materiale decalcomania.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
TQID: 'https://experienceleague.adobe.com/HLyEmmOch9kiHQ3sqpvHCQiHOBltjQcsZaDu0na1-Ww'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 217
ht-degree: 4%

---

# Dimensione{#size}

Dimensione decalcomania. Larghezza, altezza e spessore di un oggetto materiale decalcomania.

## Proprietà {#section-967bf1112eec4032a91ed0c8a7b10a07}

Tre numeri reali separati da virgole. Non deve essere negativo. Imposta i valori non utilizzati su 0. È possibile omettere gli zeri finali.

Specificate sia la larghezza che l&#39;altezza solo se l&#39;immagine deve essere allungata per adattarsi alle dimensioni specificate (le proporzioni potrebbero cambiare). Impostate la larghezza o l&#39;altezza per ridimensionare l&#39;immagine in modo proporzionale. Impostare larghezza e altezza su 0 per utilizzare `catalog::Resolution` per determinare la dimensione dell&#39;oggetto.

Fornite un valore di spessore per aggiungere un&#39;ombra esterna all&#39;oggetto decalcomania. Facoltativo per i materiali di decalcomania, ignorato da tutti gli altri materiali.

## Predefinito {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Questo indica che la dimensione della decalcomania deve essere determinata in base a catalog::Resolution e che l&#39;oggetto non ha uno spessore (quindi non viene riprodotta alcuna ombra esterna).

## Esempi {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>La decalcomania è costretta a 12x3 pollici di dimensioni e non ha spessore (questo è, senza ombra goccia). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>La decalcomania è larga 5 pollici, l'altezza è determinata dalle proporzioni dell'immagine e un'ombra esterna viene riprodotta in base a uno spessore di 1 pollice. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>La larghezza e l'altezza della decalcomania sono determinate da catalog::Resolution e che lo spessore della decalcomania sia di ½ pollice. </p></td> 
 </tr> 
</table>

## Consultate anche {#section-31a164e781d14e92bd9d379d3c329e92}

[catalogo::Risoluzione](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
