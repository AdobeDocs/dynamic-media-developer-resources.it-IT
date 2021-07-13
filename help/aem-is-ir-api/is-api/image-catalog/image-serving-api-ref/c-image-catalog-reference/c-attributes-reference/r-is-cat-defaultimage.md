---
description: Immagine di risposta predefinita. Specifica l'immagine o la voce di catalogo da utilizzare nel caso in cui non sia possibile trovare un file di immagine e defaultImage= non sia specificato nella richiesta.
solution: Experience Manager
title: DefaultImage
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# DefaultImage{#defaultimage}

Immagine di risposta predefinita. Specifica l&#39;immagine o la voce di catalogo da utilizzare nel caso in cui non sia possibile trovare un file di immagine e defaultImage= non sia specificato nella richiesta.

Può trattarsi di una voce di catalogo (incluso un modello) o di un relativo (a `attribute::RootPath`) o di un percorso di file di immagine assoluto. Utile per sostituire le immagini mancanti con le immagini predefinite.

## Proprietà {#section-b6d8193827c34e5f948792aba8b8daaf}

Stringa di testo. Se specificato, deve essere un valore `catalog::Id` valido in questo catalogo immagini o un percorso relativo (a `attribute::RootPath`) o assoluto a un file immagine accessibile dal server immagini.

## Restrizioni {#section-5d8ea872f0b0415fbd3a83410bbcf512}

Le sorgenti di immagine esterne non sono coperte dal meccanismo di immagine predefinito; se un&#39;origine immagine esterna non è valida, viene restituito un errore.

## Predefinito {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

Ereditato da `default::DefaultImage` se non definito. Se definito ma vuoto, il comportamento predefinito dell’immagine viene disattivato, anche se è definito `default::DefaultImage` .

## Consultate anche {#section-dc0fb4e72294442882b33a479fbc2b82}

[attributo::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [catalogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [attributo::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c),  [attributo::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
