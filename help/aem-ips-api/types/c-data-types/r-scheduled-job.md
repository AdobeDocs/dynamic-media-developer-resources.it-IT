---
description: Un processo pianificato per l'esecuzione.
seo-description: Un processo pianificato per l'esecuzione.
seo-title: ScheduledJob
solution: Experience Manager
title: ScheduledJob
topic: Dynamic Media Image Production System API
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 3%

---


# ScheduledJob{#scheduledjob}

Un processo pianificato per l&#39;esecuzione.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Maniglia aziendale. |
| `*`jobHandle`*` | `xsd:string` | Handle processo pianificato. |
| `*`name`*` | `xsd:string` | Nome processo. |
| `*`OriginalName`*` | `xsd:string` | Nome originale del processo pianificato. |
| `*`type`*` | `xsd:string` | Tipo di processo. |
| `*`submitUserEmail`*` | `xsd:string` | L’indirizzo e-mail dell’utente che ha pianificato il processo. |
| `*`locale`*` | `xsd:string` | Le impostazioni internazionali da utilizzare per i dettagli del registro dei processi e per la localizzazione delle e-mail. Le impostazioni internazionali sono specificate come `<language_code>[- <country_code>]`, dove il codice della lingua è un codice di due lettere minuscoli, come specificato dallo standard ISO-639, e il codice del paese facoltativo è un codice di due lettere maiuscole, come specificato dallo standard ISO-3166. Ad esempio, la stringa per l&#39;inglese (Stati Uniti) è: `en-US`. |
| `*`description`*` | `xsd:string` | Una descrizione del processo come specificato originariamente in `submitJob`. |
| `*`execSchedule`*` | `xsd:string` | Quando è pianificato l&#39;esecuzione del processo. |
| `*`nextFireTime`*` | `xsd:dateTime` | Data, ora e fuso orario in cui verrà avviato il processo. |
| `*`timeZone`*` | `xsd:dateTime` | Fuso orario del processo pianificato. |
| `*`triggerState`*` | `xsd:int` | Scelta dello stato di attivazione del processo. |
| `*`imageServingPublishJob`*` | `types:ImageServingPublishJob` | Dettagli del processo per un processo di pubblicazione di Image Server. |
| `*`imageServingRenderJob`*` | `types:ImageServingRenderJob` | Dettagli del processo per un processo di rendering delle immagini. |
| `*`videoPublishJob`*` | `types:VideoPublishJob` | Dettagli del processo per un processo di pubblicazione video. Vedere [VideoPublishJob](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| `*`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | Dettagli del processo per un processo di pubblicazione della directory del server. |
| `*`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | Dettagli del processo per un processo della directory di caricamento. |
| `*`uploadUrlsJob`*` | `types:UploadUrlsJob` | Dettagli processo per un processo URL di caricamento. |
| `*`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| `*`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| `*`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| `*`exportJob`*` | `types:ExportJob` | Consenti esportazione autorizzata di file caricati in precedenza. Vedere [Processo di esportazione](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Note {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Quando si specifica un valore per il tipo di processo in `submitJob`, il sistema restituisce un processo in base a tale tipo. È possibile restituire i seguenti processi:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

