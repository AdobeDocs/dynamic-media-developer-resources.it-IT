---
description: Vengono descritti i tipi di dati nuovi e modificati per la versione 4.2 dell'API IPS.
solution: Experience Manager
title: Tipi di dati Nuovo e Modified (Tipi di dati  e modificati)
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 0%

---

# Tipi di dati: Nuovo e Modified (Modificati){#data-types-new-and-modified}

Vengono descritti i tipi di dati nuovi e modificati per la versione 4.2 dell&#39;API IPS.

Sintassi

## Tipi di Nuovo {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## Tipi modificati {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**Bene**

Parametri aggiunti:

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

Parametri rimossi:

* `ImageSetInfo`
* `RenderSetInfo`

**ReprocessAssetsJob**

Parametri aggiunti:

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**Processo di caricamento directory**

Parametri aggiunti:

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**Carica URL processo**

Parametri aggiunti:

* `preservePublishState`
* `preserveCrop`
