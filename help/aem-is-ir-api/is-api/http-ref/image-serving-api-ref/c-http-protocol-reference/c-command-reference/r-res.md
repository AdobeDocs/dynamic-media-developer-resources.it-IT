---
description: Ridimensionamento delle immagini basato sulla risoluzione. Consente di ridimensionare l’immagine in base alla risoluzione richiesta.
seo-description: Ridimensionamento delle immagini basato sulla risoluzione. Consente di ridimensionare l’immagine in base alla risoluzione richiesta.
seo-title: res
solution: Experience Manager
title: res
topic: Dynamic Media Image Serving - Image Rendering API
uuid: ab0c8329-5d40-4233-a122-8cb8ca01b500
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---


# res{#res}

Ridimensionamento delle immagini basato sulla risoluzione. Consente di ridimensionare l’immagine in base alla risoluzione richiesta.

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>risoluzione di destinazione; in genere in pixel per pollice (reale). </p> </td> 
 </tr> 
</table>

Il fattore di scala è calcolato dividendo *`val`* per `catalog::Resolution`. Questo comando non influisce sulla risoluzione di stampa dell&#39;immagine di risposta.

Per utilizzare questa funzione, la risoluzione delle immagini sorgente originali deve essere nota e impostata in `catalog::Resolution`. A seconda dell&#39;applicazione, le unità di risoluzione possono variare. Per texture o campioni di materiale ripetibili in 2D, come sfondi o tessuti, la risoluzione può essere espressa in pixel/pollice o in pixel/mm. Le foto e le mappe aeree possono essere meglio servite da pixel/miglia o pixel/km. In ogni caso, le unità utilizzate per `catalog::Resolution` devono essere le stesse utilizzate per `res=`.

Oltre a ottenere immagini a risoluzioni precise, `res=` può essere utilizzato anche per combinare più immagini alla stessa risoluzione, in modo che gli elementi visibili in queste immagini siano in proporzione precisa l&#39;uno all&#39;altro.

>[!NOTE]
>
>Normalmente, un&#39;immagine composita viene ridimensionata in base alle dimensioni della visualizzazione di destinazione (specificate da `wid=`, `hei=` o `attribute::DefaultPix`) prima che venga restituita al client. Per impedire che questo venga ridimensionato e ottenere un&#39;immagine con la risoluzione esatta specificata da `res=`, potrebbe essere necessario disattivare il ridimensionamento della vista specificando esplicitamente `scl=1`. Questo indica al server di ritagliare l&#39;immagine composita alla dimensione della visualizzazione di destinazione anziché ridimensionarla.

## Proprietà {#section-fdbd16e59cff4952a3717146bc91412e}

Attributo immagine/maschera di origine. Ignorato dai livelli non associati a un’immagine o maschera sorgente. Applicato al livello 0 è specificato per `layer=comp`. Ignorato se per lo stesso livello è specificato `scale=` o `size=`.

## Predefinito {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

Se non viene specificato, il fattore di scala è determinato da `scale=` o `size=` oppure, se non viene specificato nessuno, l&#39;immagine viene utilizzata senza essere ridimensionata.

## Esempio {#section-eb06f333e08e4247971fb1b18922597b}

Recuperate un’immagine di texture con una risoluzione di 12 pixel/pollice per l’utilizzo con il rendering delle immagini o l’authoring delle immagini. È possibile specificare un formato PNG senza perdita di dati e un ricampionamento di qualità migliore per ottenere la migliore qualità possibile,

` http:// *`server`*/myTexture?res=12&fmt=png&resMode=sharp`

## Consultate anche {#section-1f8a8f11772e493ca803c4511f397a11}

[catalogo::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1) ,  [attributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
