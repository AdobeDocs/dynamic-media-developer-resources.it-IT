---
description: Percorso radice dati di origine. Percorso assoluto o relativo per la cartella principale dei dati di origine del catalogo immagini.
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# RootPath{#rootpath}

Percorso radice dati di origine. Percorso assoluto o relativo per la cartella principale dei dati di origine del catalogo immagini.

Il `RootPath` è un valore di stringa di testo. Per ulteriori informazioni sui percorsi radice del server, consulta [Gestione dei dati di origine](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) .

## Proprietà {#section-b41d7e0ea63143eb8034569706cad0c0}

Stringa di testo. Deve essere vuoto, un percorso di cartella relativo valido o un percorso assoluto valido accessibile dal server di immagini.

## Predefinito {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Ereditato da `default::RootPath` se non definito. Se definito ma vuoto, non contribuirà al percorso principale del file di origine.

## Consultate anche {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalogo::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),   [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e),  [Managing Source Data](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
