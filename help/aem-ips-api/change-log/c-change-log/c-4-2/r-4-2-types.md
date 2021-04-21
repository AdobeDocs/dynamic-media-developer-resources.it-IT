---
description: Descrive i tipi di dati nuovi e modificati per l’API IPS versione 4.2.
solution: Experience Manager
title: Tipi di dati nuovi e modificati
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 1%

---


# Tipi di dati: Nuovo e modificato{#data-types-new-and-modified}

Descrive i tipi di dati nuovi e modificati per l’API IPS versione 4.2.

Sintassi

## Nuovi tipi {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## Tipi modificati {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**Risorsa**

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

**UploadDirectoryJob**

Parametri aggiunti:

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

Parametri aggiunti:

* `preservePublishState`
* `preserveCrop`

