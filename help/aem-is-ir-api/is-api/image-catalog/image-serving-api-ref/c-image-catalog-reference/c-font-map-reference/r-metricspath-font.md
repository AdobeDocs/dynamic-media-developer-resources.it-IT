---
description: Percorso del file delle metriche dei font. Percorso e nome di un file di metriche dei caratteri, incluso il suffisso file.
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0f1f98a5-b53b-4e20-b4c8-e70482b01a04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---

# MetricsPath{#metricspath}

Percorso del file delle metriche dei font. Percorso e nome di un file di metriche dei caratteri, incluso il suffisso file.

Utilizzato per i font Adobe Type 1. Se non viene specificato diversamente, il server tenterà di trovare un file di metriche dei caratteri nella stessa cartella in cui si trova il file dei caratteri principale. Se al momento del rendering non è possibile trovare un file di metriche dei font richiesto, si verifica un errore.

## Proprietà {#section-955268c581574875b05253d9e14544f3}

Stringa di testo. Facoltativo per i file Adobe Type 1. Deve essere vuoto o un percorso di file del server immagini valido, assoluto o relativo a `attribute::RootPath`.

## Predefinito {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Nessuno.

## Consultate anche {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
