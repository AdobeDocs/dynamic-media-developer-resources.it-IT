---
description: Lucidità superficie Consente di specificare la lucidità relativa della superficie del materiale.
solution: Experience Manager
title: Lucentezza
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
TQID: 'https://experienceleague.adobe.com/Q1mOPjFXFnSPVRsvYpKs3a-15g1BfxQRCsFaMRBZNTw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 2%

---

# Lucentezza{#gloss}

Lucidità superficie Consente di specificare la lucidità relativa della superficie del materiale.

Questo valore viene utilizzato dal renderer per i seguenti scopi:

* Selezionare la mappa di illuminazione quando `catalog::Illum` è -1.
* Controlla il rendering dell&#39;effetto lucentezza (riflessione speculare) insieme a `catalog::Type`.
* Controlla gli effetti di rendering della riflessione 3D insieme a `catalog::Type` e `catalog::Roughness`.

## Proprietà {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Numero intero. Numero percentuale nell&#39;intervallo 0...100. Facoltativo per tutti i materiali. Utilizzato solo per vignettature con più mappe di riflessione o vignettature con funzionalità di riflessione 3D. Lascia vuoto o imposta su -1 se non noto o non necessario.

## Predefinito {#section-2352721073524f1a8d461f64a363aac9}

Se questo valore è impostato su -1, la vignettatura fornisce un valore predefinito.

## Consultate anche {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalogo::rugosità](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalogo::Tipo](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
