---
description: Rugosità della superficie. Specifica la lucentezza relativa della superficie del materiale. Utilizzato in combinazione con il tipo di catalogo e la brillantezza del catalogo per controllare gli effetti di rendering della riflessione 3D.
solution: Experience Manager
title: Rugosità
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
TQID: 'https://experienceleague.adobe.com/YvUmUkOLzzbM7Zs-7T35rwYRNrUeh6-QXW339AA3R8Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 2%

---

# Rugosità{#roughness}

Rugosità della superficie. Specifica la lucentezza relativa della superficie del materiale. Utilizzato insieme a catalog::Type e catalog::Gloss per controllare gli effetti di rendering della riflessione 3D.

## Proprietà {#section-70c3f2394fd8477ca83a369448907971}

Numero intero. Valore percentuale compreso nell&#39;intervallo 0...100. Facoltativo per tutti i materiali. Utilizzato solo per vignettature con più mappe di riflessione o vignettature con funzionalità di riflessione 3D. Lascia vuoto o imposta su -1 se non noto o non necessario.

## Predefinito {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; viene utilizzato un server predefinito.

## Consultate anche {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , [catalogo::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [catalogo::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
