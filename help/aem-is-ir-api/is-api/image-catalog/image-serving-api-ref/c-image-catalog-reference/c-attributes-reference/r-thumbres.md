---
description: Risoluzione predefinita delle miniature. Fornisce un valore predefinito per la risoluzione dell'oggetto miniatura nel caso in cui un particolare record di catalogo non contenga un valore ThumbRes di catalogo valido.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# ThumbRes{#thumbres}

Risoluzione predefinita delle miniature. Fornisce un valore predefinito per la risoluzione dell&#39;oggetto miniatura nel caso in cui un particolare record di catalogo non contenga un valore di catalogo valido::ThumbRes.

Utilizzato solo per le richieste di miniature ( `req=tmb`) e quando `catalog::ThumbType=3`.

## Proprietà {#section-88d37d0e030f4879a9e584dd2cc780f3}

Numero reale, maggiore di 0.Tipicamente espresso in pixel per pollice, ma può anche essere in altre unità, come i pixel per metro.

## Predefinito {#section-86588899ec9b4276a98b03d7faf64003}

Ereditato da `default::ThumbRes` se non definito o se vuoto.

## Consultate anche {#section-a6d2cce2e404441a996dba98a95c8e16}

[catalogo::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
