---
description: Dimensione del carrello. Larghezza, altezza e spessore di un oggetto materiale cardine.
seo-description: Dimensione del carrello. Larghezza, altezza e spessore di un oggetto materiale cardine.
seo-title: Dimensione
solution: Experience Manager
title: Dimensione
topic: Scene7 Image Serving - Image Rendering API
uuid: 07d41f71-e18d-4559-afc7-75dc1c45be93
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 4%

---


# Dimensione{#size}

Dimensione del carrello. Larghezza, altezza e spessore di un oggetto materiale cardine.

## Proprietà {#section-967bf1112eec4032a91ed0c8a7b10a07}

Tre numeri reali separati da virgole. Non deve essere negativo. Impostate i valori non utilizzati su 0. Gli zeri finali possono essere omessi.

Specificate larghezza e altezza solo se l’immagine deve essere allungata per adattarsi alle dimensioni specificate (le proporzioni potrebbero variare). Impostare larghezza o altezza per ridimensionare l’immagine in modo proporzionale. Impostare larghezza e altezza su 0 per utilizzare `catalog::Resolution`per determinare le dimensioni dell&#39;oggetto.

Specificare un valore di spessore per aggiungere un&#39;ombra esterna all&#39;oggetto decal. Facoltativo per i materiali di decallo, ignorati da tutti gli altri materiali.

## Predefinito {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Questo indica che la dimensione del decal deve essere determinata in base al catalogo::Resolution, e che l&#39;oggetto non ha uno spessore (pertanto non verrà eseguito il rendering dell&#39;ombra esterna).

## Esempi {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>Il decal è forzato a 12x3 pollici di dimensione e non ha spessore (ovvero, nessuna ombra esterna). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>L'ingombro è di 5 pollici di larghezza, l'altezza è determinata dalle proporzioni dell'immagine, e un'ombra esterna è rappresentata da uno spessore di 1 pollice. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,5 </p></td> 
  <td class="stentry"> <p>La larghezza e l'altezza del decallo sono determinate dal catalogo::Resolution e lo spessore è di ½ pollice. </p></td> 
 </tr> 
</table>

## Consultate anche {#section-31a164e781d14e92bd9d379d3c329e92}

[catalogo:Risoluzione](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
