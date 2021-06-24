---
description: Descrive i tipi di dati nuovi e modificati per l’API IPS versione 4.2.
solution: Experience Manager
title: Tipi di dati nuovi e modificati
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '56'
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
