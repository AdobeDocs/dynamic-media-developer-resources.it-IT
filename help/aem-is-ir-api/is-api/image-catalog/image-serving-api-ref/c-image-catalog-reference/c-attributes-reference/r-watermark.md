---
description: Selettore filigrana. Specifica l'ID del catalogo del record del catalogo da utilizzare come immagine o modello di filigrana.
seo-description: Selettore filigrana. Specifica l'ID del catalogo del record del catalogo da utilizzare come immagine o modello di filigrana.
seo-title: Filigrana
solution: Experience Manager
title: Filigrana
uuid: 18add7ab-0797-4ab3-a7e8-05c745abe605
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 5%

---


# Filigrana{#watermark}

Selettore filigrana. Specifica il catalogo::Id del record del catalogo da utilizzare come immagine o modello di filigrana.

Se specificato, il server applica la filigrana ai dati immagine richiesti per tutte le richieste di immagini ( `req=img`).

## Proprietà {#section-fad6ffff4c5f4b5c8010281bc1377055}

Stringa di testo. Se specificato, deve essere un valore `Catalog::Id` valido in questo catalogo immagini (o nel catalogo predefinito, se specificato in [!DNL default.ini]).

## Predefinito {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Ereditato da `default::Watermark` se non definito. Se definito ma vuoto, non viene applicato alcun watermarking per questo catalogo di immagini, anche se è definito `default::Watermark`.

## Consultate anche {#section-f15dbe31013849828d78588742dde58e}

[catalogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
