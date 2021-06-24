---
description: Rugosità della superficie. Specifica la lucentezza relativa della superficie del materiale. Utilizzato in combinazione con Tipo catalogo e Gloss catalogo per controllare gli effetti di rendering di riflesso 3D.
solution: Experience Manager
title: Rugosità
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---

# Rugosità{#roughness}

Rugosità della superficie. Specifica la lucentezza relativa della superficie del materiale. Utilizzato in combinazione con catalog::Type e catalog::Gloss per controllare gli effetti di rendering del riflesso 3D.

## Proprietà {#section-70c3f2394fd8477ca83a369448907971}

Numero intero. Valore percentuale nell&#39;intervallo 0...100. Facoltativo per tutti i materiali. Utilizzato solo per vignette con mappe di riflesso multiple o vignette con capacità di riflessione 3D. Lasciare vuoto o impostare su -1 se non noto o non necessario.

## Predefinito {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; viene utilizzato un server predefinito.

## Consultate anche {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[grezzo=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) ,  [catalogo::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb),  [catalogo::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
