---
description: Tipo di miniatura. Descrive come generare una miniatura per questa immagine.
solution: Experience Manager
title: ThumbType
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---


# ThumbType{#thumbtype}

Tipo di miniatura. Descrive come generare una miniatura per questa immagine.

Sono supportati i seguenti tipi di miniature:

<table id="simpletable_874E4190A1DC4FB0AE1B2E3734746527"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Ritaglio (1) </p></td> 
  <td class="stentry"> <p>Ritaglia l’immagine in base alle proporzioni delle miniature. A meno che le proporzioni del rettangolo della miniatura e dell'immagine non siano esattamente uguali, una parte dell'immagine viene ritagliata per assicurarsi che l'intero rettangolo della miniatura sia riempito con i dati dell'immagine. Il rettangolo di ritaglio è posizionato nell'immagine utilizzando l'attributo <span class="codeph">::ThumbHorizAlign</span> e l'attributo <span class="codeph">::ThumbVertAlign</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Adatta (2) </p></td> 
  <td class="stentry"> <p>Adattare l'intera immagine al rettangolo della miniatura. L'immagine è posizionata all'interno del rettangolo delle miniature utilizzando l'attributo <span class="codeph">::ThumbHorizAlign</span> e l'attributo <span class="codeph">::ThumbVertAlign</span> e qualsiasi spazio aggiuntivo è riempito con l'attributo <span class="codeph">::ThumbBkgColor</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Texture (3) </p></td> 
  <td class="stentry"> <p>Ritaglia l'immagine in base alla risoluzione. L'immagine viene ridimensionata in base al rapporto tra <span class="codeph"> catalogo::ThumbRes</span> e <span class="codeph"> catalogo::Resolution</span>. Se l'immagine risultante è più grande della miniatura, viene ritagliata per adattarsi, se l'immagine in scala è più piccola della miniatura, l'area rimanente viene riempita con l'attributo <span class="codeph">::ThumbBkgColor</span>. <span class="codeph"> attributo: </span> ThumbHorizAlignand  <span class="codeph"> attribute::</span> ThumbVertAlignare utilizzato per determinare la posizione del rettangolo di ritaglio all’interno di un’immagine più grande o la posizione di un’immagine più piccola all’interno della miniatura. </p></td> 
 </tr> 
</table>

I clienti richiedono miniature di immagine con richieste `req=tmb` .

## Proprietà {#section-c58a8e67c2134ca3a0edd21b20dd3052}

Valore enum. I valori validi sono 1, 2 o 3, che corrispondono rispettivamente ai tipi di ritaglio, Fit e Texture.

## Predefinito {#section-a6a7c43a83384a4aab861a48d73c7c26}

`attribute::ThumbType` viene utilizzato se il campo non è presente, se il valore è 0 o se il campo è vuoto.

## Consultate anche {#section-fc1a79d3e6274b4381a17da159649a07}

[attributo::ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbtype.md#reference-329e9dbf3e5f49548d1eb61915b538f5) ,  [attributo::ThumbBkgColor](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbbkgcolor.md#reference-8e38088e79a54446a9106d0b93c9b31e),  [attributo::ThumbHorizAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbhorizalign.md#reference-0ae8b88669df4769a9053b22aca33691),  [attributo::ThumbVertAlign](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbvertalign.md#reference-d47c6b34588c4855b04ad134e472f04f),  [catalogo::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69),  [catalogo::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1),  [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [ThumbScaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
