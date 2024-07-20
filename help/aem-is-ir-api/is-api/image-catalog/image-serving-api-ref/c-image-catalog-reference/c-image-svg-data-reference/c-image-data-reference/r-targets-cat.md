---
description: Zoom dei dati di destinazione. Nessuna o più proprietà della destinazione di zoom, che possono essere utilizzate insieme al client del visualizzatore di zoom.
solution: Experience Manager
title: Target
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# Target{#targets}

Zoom dei dati di destinazione. Nessuna o più proprietà della destinazione di zoom, che possono essere utilizzate insieme al client del visualizzatore di zoom.

Il server restituisce il contenuto di questo campo in risposta a `req=targets`, dopo aver sostituito i token di terminazione dei record &#39;`??`&#39;.

Ad ogni destinazione di zoom possono essere associate fino a quattro proprietà:

` Target. *`num`*.frame= *`fotogramma`*`

` Target. *`num`*.rect= *`sinistra,alto,larghezza,altezza`*`

` Target. *`num`*.label= *`etichetta`*`

` Target. *`num`*.userData= *`datiUtente`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span> </span> </p> </td> 
  <td class="stentry"> <p>Numero destinazione di zoom (int); le destinazioni di zoom devono essere numerate in sequenza e in sequenza, a partire da 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> frame </span> </span> </p> </td> 
  <td class="stentry"> <p>Numero di frame/pagina facoltativo per il targeting di un frame/pagina specifico di un set 360 gradi o di una brochure. Se non è specificato per l'uso del visualizzatore rotazione e brochure, il valore predefinito è 0. Viene ignorato dal visualizzatore zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rimasti, primi </span> </span> </p> </td> 
  <td class="stentry"> <p>Offset pixel dal margine superiore sinistro dell'immagine al margine superiore sinistro del rettangolo di destinazione dello zoom (int, int); deve essere maggiore o uguale a 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> larghezza, altezza </span> </span> </p> </td> 
  <td class="stentry"> <p>Dimensione in pixel del rettangolo di destinazione dello zoom (int, int); deve essere maggiore di 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> etichetta </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore di dati di testo; può essere utilizzato come etichetta di testo per un collegamento di destinazione di zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> dati utente </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore di dati di testo; può essere utilizzato per trasmettere al client informazioni specifiche per la destinazione, ad esempio un valore SKU o un URL di collegamento rapido. </p> </td> 
 </tr> 
</table>

Target. *`num`*.rect è obbligatorio per ogni destinazione di zoom e deve specificare un rettangolo all&#39;interno dell&#39;immagine. Tutte le altre proprietà sono facoltative.

*`label`* e *`userData`* partecipano alla localizzazione delle stringhe di testo. Per ulteriori informazioni, consultare [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) nella *documentazione sul protocollo HTTP*.

Per le applicazioni che coinvolgono i client visualizzatore di rotazioni e brochure, le destinazioni di zoom devono essere definite nello stesso record di catalogo che definisce il set di immagini. Qualsiasi definizione di destinazione di zoom nei record di catalogo dei membri del set di immagini viene ignorata dal visualizzatore.

I visualizzatori Dynamic Medie prevedono destinazioni di zoom nelle coordinate dell&#39;immagine a risoluzione completa già regolate dai comandi di `catalog::Modifier`.

## Proprietà {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Valore dati proprietà](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md).

## Predefinito {#section-feab29f6575e482391086a57f547543c}

Nessuno.

## Consultate anche {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalogo::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalogo::Modificatore](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Localizzazione stringa di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
