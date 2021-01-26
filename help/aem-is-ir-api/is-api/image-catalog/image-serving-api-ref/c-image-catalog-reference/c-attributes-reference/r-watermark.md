---
description: Selettore filigrana. Specifica l'ID catalogo del record catalogo da utilizzare come immagine o modello di filigrana.
seo-description: Selettore filigrana. Specifica l'ID catalogo del record catalogo da utilizzare come immagine o modello di filigrana.
seo-title: Filigrana
solution: Experience Manager
title: Filigrana
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 18add7ab-0797-4ab3-a7e8-05c745abe605
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 5%

---


# Filigrana{#watermark}

Selettore filigrana. Specifica il catalogo::Id del record del catalogo da utilizzare come immagine o modello di filigrana.

Se specificato, il server applica la filigrana ai dati immagine richiesti per tutte le richieste di immagini ( `req=img`).

## Proprietà {#section-fad6ffff4c5f4b5c8010281bc1377055}

Stringa di testo. Se specificato, deve essere un valore `Catalog::Id` valido in questo catalogo immagini (o nel catalogo predefinito, se specificato in [!DNL default.ini]).

## Predefinito {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Ereditato da `default::Watermark` se non definito. Se definito ma vuoto, non viene applicata alcuna filigrana al catalogo immagini, anche se è definito `default::Watermark`.

## Consultate anche {#section-f15dbe31013849828d78588742dde58e}

[catalogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
