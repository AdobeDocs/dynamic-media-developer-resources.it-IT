---
description: Lucidità superficie Specifica la lucentezza relativa della superficie del materiale.
solution: Experience Manager
title: Glossario
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# Glossario{#gloss}

Lucidità superficie Specifica la lucentezza relativa della superficie del materiale.

Questo valore viene utilizzato dal renderer per i seguenti scopi:

* Selezionare la mappa di illuminazione quando `catalog::Illum` è -1.
* Controlla il rendering dell&#39;effetto lucido (riflesso speculare) in combinazione con `catalog::Type`.
* Controlla gli effetti di rendering del riflesso 3D in combinazione con `catalog::Type` e `catalog::Roughness`.

## Proprietà {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Numero intero. Numero percentuale nell&#39;intervallo 0...100. Facoltativo per tutti i materiali. Utilizzato solo per vignette con mappe di riflesso multiple o vignette con capacità di riflessione 3D. Lasciare vuoto o impostare su -1 se non noto o non necessario.

## Predefinito {#section-2352721073524f1a8d461f64a363aac9}

Se questo valore è impostato su -1, la vignetta fornisce un valore predefinito.

## Consultate anche {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ,  [catalogo::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99),  [catalogo::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
