---
title: Gestione caratteri
description: Tutti i font a cui si fa riferimento nella stringa RTF devono essere disponibili nel file di mappa font del catalogo predefinito o del catalogo immagine corrente. In caso contrario viene restituito un errore.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e8e3ce9850ab8059aed81e720574d0c93f867a22
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Gestione caratteri{#font-handling}

Tutti i font a cui si fa riferimento nella stringa RTF devono essere disponibili nel file di mappa font del catalogo predefinito o del catalogo immagine corrente. In caso contrario viene restituito un errore.

La migliore qualità per il testo in corsivo e in grassetto si ottiene registrando i file di font corrispondenti. Se non è disponibile, il server è in grado di sintetizzare i caratteri in grassetto e/o corsivo del volto standard. (vedere [attribute::SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

Il tipo di carattere specificato con `attribute::DefaultFont` viene utilizzato quando nessuno è specificato esplicitamente nella stringa RTF.

Image Server supporta i caratteri TrueType® OpenType e Adobi Type 1 (solo Windows).

<!-- THIS APPEARS TO BE VERY OLD OUTDATED INFORMATION; URL IS DEAD TOO ## Photofont&reg; font support {#section-74560ae898cf4708aba4c8b4093f5f00}

Photofont&reg; fonts support `textPs=`, with the following restrictions:

* `\cf` is ignored in text spans that specify a Photofont font; Photofont font faces have predefined colors 
* Synthesized font styles are not supported; use of `\b` and `\i`require corresponding font map entries, otherwise an error is returned 

* Vertical text flow is not supported 
* Photofont fonts with 16-bit images are not supported 
* Photofont fonts with multiple glyphs per image are not supported 
* Naïve color conversion is applied unless the Photofont glyph images embed color profiles; in this case, relative colorimetric render intent and blackpoint compensation are always applied

See [https://www.photofont.com](https://www.photofont.com) for additional information. -->

## Consultate anche {#section-6cb8a802aa044836bbe449d559093f3a}

[Riferimento mappa font](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)
