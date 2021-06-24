---
description: Selettore filigrana. Specifica l'ID del catalogo del record del catalogo da utilizzare come immagine o modello di filigrana.
solution: Experience Manager
title: Filigrana
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
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
