---
description: Percorso del file delle metriche dei font. Percorso e nome di un file di metriche dei font, incluso il suffisso del file.
seo-description: Percorso del file delle metriche dei font. Percorso e nome di un file di metriche dei font, incluso il suffisso del file.
seo-title: MetricsPath
solution: Experience Manager
title: MetricsPath
topic: Scene7 Image Serving - Image Rendering API
uuid: b59110bf-330f-4ca4-8b0a-219a61d383f7
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# MetricsPath{#metricspath}

Percorso del file delle metriche dei font. Percorso e nome di un file di metriche dei font, incluso il suffisso del file.

Utilizzata per i font Adobe Type 1. Se non viene specificato, il server tenterà di trovare un file di metriche dei font nella stessa cartella in cui si trova il file di font principale. Se in fase di rendering non è possibile trovare un file di metriche di font richiesto, si verificherà un errore.

## Proprietà {#section-955268c581574875b05253d9e14544f3}

Stringa di testo. Facoltativo per i file Adobe Type 1. Deve essere vuoto o un percorso di file valido per Image Server, assoluto o relativo a `attribute::RootPath`.

## Predefinito {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Nessuno.

## Consultate anche {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
