---
description: Tutti i font a cui si fa riferimento nella stringa RTF devono essere disponibili nel file mappa font del catalogo predefinito o del catalogo immagini corrente, altrimenti viene restituito un errore.
solution: Experience Manager
title: Gestione dei font
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Gestione dei font{#font-handling}

Tutti i font a cui si fa riferimento nella stringa RTF devono essere disponibili nel file mappa font del catalogo predefinito o del catalogo immagini corrente, altrimenti viene restituito un errore.

La migliore qualità del testo in corsivo e in grassetto viene ottenuta registrando i corrispondenti file di font. Se non disponibile, il server può sintetizzare le facce di font in grassetto e/o corsivo dalla faccia standard. (Vedere ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`.)

La faccia di font specificata con `attribute::DefaultFont` viene utilizzata quando non è specificata esplicitamente nella stringa RTF.

Image Server supporta i font TrueType, OpenType, Adobe Type 1 (solo Windows).

## Supporto font Photofont® {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` supporta i font Photofont®, con le seguenti limitazioni:

* `\cf` viene ignorato nelle aree di testo che specificano un font Photofont; Le facce font a forma di foto hanno colori predefiniti
* Gli stili di font sintetizzati non sono supportati; l&#39;utilizzo di `\b` e `\i`richiede le voci corrispondenti della mappa dei font, altrimenti viene restituito un errore

* Il flusso verticale del testo non è supportato
* I font Photofont con immagini a 16 bit non sono supportati
* I font Photofont con più glifi per immagine non sono supportati
* Viene applicata una conversione del colore ingenua a meno che le immagini del glifo Photofont non incorporino profili di colore; in questo caso, vengono sempre applicati l’intento di rendering colorimetrico relativo e la compensazione del punto nero

Per ulteriori informazioni, fare riferimento a ` [www.photofont.com](http://www.photofont.com)` .

## Consultate anche {#section-6cb8a802aa044836bbe449d559093f3a}

[Riferimento](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d) mappa font,  [attributo::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15),  [attributo::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107),  [ [!DNL www.photofont.com] ](http://www.photofont.com)
