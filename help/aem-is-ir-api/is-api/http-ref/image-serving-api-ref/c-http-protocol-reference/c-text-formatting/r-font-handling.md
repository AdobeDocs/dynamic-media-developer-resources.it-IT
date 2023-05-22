---
title: Gestione caratteri
description: Tutti i font a cui si fa riferimento nella stringa RTF devono essere disponibili nel file di mappa font del catalogo predefinito o del catalogo immagine corrente. In caso contrario viene restituito un errore.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e1f0f8bdac2b7a8397adac3bb9ba38d0c519f8fb
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Gestione caratteri{#font-handling}

Tutti i font a cui si fa riferimento nella stringa RTF devono essere disponibili nel file di mappa font del catalogo predefinito o del catalogo immagine corrente. In caso contrario viene restituito un errore.

La migliore qualità per il testo in corsivo e in grassetto si ottiene registrando i file di font corrispondenti. Se non è disponibile, il server è in grado di sintetizzare i caratteri in grassetto e/o corsivo del volto standard. (vedere [attribute::SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

Il tipo di carattere specificato con `attribute::DefaultFont` viene utilizzato quando nessuno è specificato esplicitamente nella stringa RTF.

Image Server supporta i caratteri TrueType, OpenType e Adobe Type 1 (solo Windows).

## Supporto per i caratteri Photofont® {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` supporta i caratteri Photofont® con le seguenti limitazioni:

* `\cf` viene ignorato negli intervalli di testo che specificano un font Photofont; le facce dei font Photofont hanno colori predefiniti
* Gli stili di carattere sintetizzati non sono supportati; utilizzo di `\b` e `\i`richiede le voci di mappa font corrispondenti, altrimenti viene restituito un errore

* Flusso di testo verticale non supportato
* I font Photofont con immagini a 16 bit non sono supportati
* I font Photofont con più glifi per immagine non sono supportati
* Viene applicata la conversione colore Naïve a meno che le immagini del glifo Photofont non incorporino profili di colore; in questo caso, vengono sempre applicati l&#39;intento di rendering colorimetrico relativo e la compensazione del punto nero

Fai riferimento a [www.photofont.com](https://www.photofont.com) per ulteriori informazioni.

## Consultate anche {#section-6cb8a802aa044836bbe449d559093f3a}

[Riferimento mappa font](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107), [ [!DNL www.photofont.com] ](https://www.photofont.com)
