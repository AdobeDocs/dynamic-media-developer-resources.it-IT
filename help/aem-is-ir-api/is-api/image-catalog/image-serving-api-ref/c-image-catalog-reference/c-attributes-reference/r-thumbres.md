---
description: Risoluzione miniature predefinita. Specifica un valore predefinito per la risoluzione degli oggetti miniatura se un record catalogo non contiene un valore ThumbRes valido per il catalogo.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# ThumbRes{#thumbres}

Risoluzione miniature predefinita. Specifica un valore predefinito per la risoluzione degli oggetti miniatura se un record catalogo non contiene un valore catalog::ThumbRes valido.

Utilizzato solo per le richieste di miniature ( `req=tmb`) e quando `catalog::ThumbType=3`.

## Proprietà {#section-88d37d0e030f4879a9e584dd2cc780f3}

Numero reale, maggiore di 0.In genere espresso come pixel per pollice, ma può anche essere espresso in altre unità, ad esempio pixel per metro.

## Predefinito {#section-86588899ec9b4276a98b03d7faf64003}

Ereditato da `default::ThumbRes` se non è definita o se è vuota.

## Consultate anche {#section-a6d2cce2e404441a996dba98a95c8e16}

[catalogo::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
