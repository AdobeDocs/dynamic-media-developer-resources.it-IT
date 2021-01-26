---
description: Descrive i tipi di dati nuovi e modificati per l'API IPS versione 4.2.
solution: Experience Manager
title: Tipi di dati nuovi e modificati
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 1%

---


# Tipi di dati: Nuovo e modificato{#data-types-new-and-modified}

Descrive i tipi di dati nuovi e modificati per l&#39;API IPS versione 4.2.

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

