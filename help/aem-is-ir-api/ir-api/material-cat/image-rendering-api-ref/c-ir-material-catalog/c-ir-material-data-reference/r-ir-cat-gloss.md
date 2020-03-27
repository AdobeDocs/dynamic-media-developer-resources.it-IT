---
description: Lucidità superficie Specifica la lucentezza relativa della superficie del materiale.
seo-description: Lucidità superficie Specifica la lucentezza relativa della superficie del materiale.
seo-title: Gloss
solution: Experience Manager
title: Gloss
topic: Scene7 Image Serving - Image Rendering API
uuid: 7db83f99-15ab-4c43-adfb-07ad0b0c9707
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Gloss{#gloss}

Lucidità superficie Specifica la lucentezza relativa della superficie del materiale.

Questo valore viene utilizzato dal renderer per i seguenti scopi:

* Selezionare la mappa di illuminazione quando `catalog::Illum` è -1.
* Controlla il rendering dell&#39;effetto lucido (riflessione speculare) insieme a `catalog::Type`.
* Controlla gli effetti di rendering del riflesso 3D insieme a `catalog::Type` e `catalog::Roughness`.

## Proprietà {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Numero intero. Numero percentuale nell’intervallo 0...100. Facoltativo per tutti i materiali. Utilizzata solo per le vignettature con mappe di riflessione multiple o vignettature con capacità di riflessione 3D. Lasciate vuoto o impostate su -1 se non noto o non necessario.

## Predefinito {#section-2352721073524f1a8d461f64a363aac9}

Un valore predefinito viene fornito dalla vignettatura se questo valore è impostato su -1.

## Consultate anche {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalogo::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalogo::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
