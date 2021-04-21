---
description: Dimensione del carrello. Larghezza, altezza e spessore di un oggetto materiale decal.
solution: Experience Manager
title: Dimensione
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 4%

---


# Dimensione{#size}

Dimensione del carrello. Larghezza, altezza e spessore di un oggetto materiale decal.

## Proprietà {#section-967bf1112eec4032a91ed0c8a7b10a07}

Tre numeri reali separati da virgole. Non deve essere negativo. Imposta i valori non utilizzati su 0. Gli zeri finali possono essere omessi.

Specificare larghezza e altezza solo se l&#39;immagine deve essere allungata per adattarsi alle dimensioni specificate (le proporzioni potrebbero cambiare). Impostare larghezza o altezza per ridimensionare l&#39;immagine proporzionalmente. Impostare sia la larghezza che l&#39;altezza su 0 per utilizzare `catalog::Resolution`per determinare le dimensioni dell&#39;oggetto.

Fornire un valore di spessore per aggiungere un&#39;ombreggiatura esterna all&#39;oggetto decal. Facoltativo per i materiali decal, ignorati da tutti gli altri materiali.

## Predefinito {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Questo indica che la dimensione del decal deve essere determinata in base al catalogo::Resolution e che l&#39;oggetto non ha uno spessore (quindi non sarà resa alcuna ombreggiatura).

## Esempi {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>La decal è forzata a 12x3 pollici in dimensioni e non ha spessore (questo è, senza ombra di goccia). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>L'decal è largo 5 pollici, l'altezza è determinata dal rapporto di formato dell'immagine e un'ombra esterna è resa in base a uno spessore di 1 pollice. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,5 </p></td> 
  <td class="stentry"> <p>La larghezza e l'altezza dell'decal sono determinate dal catalogo::Resolution e lo spessore di ½ pollice. </p></td> 
 </tr> 
</table>

## Consultate anche {#section-31a164e781d14e92bd9d379d3c329e92}

[catalogo::Risoluzione](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
