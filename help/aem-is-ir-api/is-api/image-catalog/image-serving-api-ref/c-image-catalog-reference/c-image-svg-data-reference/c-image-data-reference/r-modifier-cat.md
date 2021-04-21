---
description: Stringa modificatore richiesta prefisso. Nessuno o più comandi Image Server separati dai caratteri '&'.
solution: Experience Manager
title: Modificatore
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---


# Modificatore{#modifier}

Stringa modificatore richiesta prefisso. Nessuno o più comandi Image Server separati dai caratteri &#39;&amp;&#39;.

Utilizzato per modificare in modo permanente le immagini e memorizzare il corpo dei modelli.

I comandi in questo campo vengono ignorati dagli stessi comandi nella richiesta o nel modello a cui si fa riferimento per questo record e dai comandi in `catalog::PostModifier`

Le macro sono consentite in `catalog::Modifier`, purché siano definite nello stesso catalogo o nel catalogo predefinito. È possibile utilizzare anche variabili personalizzate.

## Proprietà {#section-6674388f77d644469371a17e8809c45f}

Stringa di testo. Facoltativo.

## Predefinito {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Nessuno.

## Consultate anche {#section-7a67803d141b442180c418c1f3cff029}

[catalogo::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
