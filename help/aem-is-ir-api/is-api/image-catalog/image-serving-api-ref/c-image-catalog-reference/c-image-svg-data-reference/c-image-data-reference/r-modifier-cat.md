---
description: Stringa modificatore richiesta prefisso. Nessuno o più comandi Image Server separati da '&' caratteri.
solution: Experience Manager
title: Modificatore
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 6%

---

# Modificatore{#modifier}

Stringa modificatore richiesta prefisso. Nessuno o più comandi Image Server separati da &#39;&amp;&#39; caratteri.

Utilizzato per modificare in modo persistente le immagini e memorizzare il corpo dei modelli.

I comandi in questo campo vengono sostituiti dagli stessi comandi nella richiesta o nel modello da cui si fa riferimento al record e dai comandi in `catalog::PostModifier`

Le macro sono consentite in `catalog::Modifier`, purché siano definite nello stesso catalogo o nel catalogo predefinito. È possibile utilizzare anche variabili personalizzate.

## Proprietà {#section-6674388f77d644469371a17e8809c45f}

Stringa di testo. Facoltativo.

## Predefinito {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Nessuno.

## Consultate anche {#section-7a67803d141b442180c418c1f3cff029}

[catalogo::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
