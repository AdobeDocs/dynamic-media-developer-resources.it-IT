---
description: Un processo pianificato per l'esecuzione.
solution: Experience Manager
title: ScheduledJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 3%

---

# ScheduledJob{#scheduledjob}

Un processo pianificato per l&#39;esecuzione.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| companyHandle | `xsd:string` | Tratta l&#39;azienda. |
| jobHandle | `xsd:string` | Handle di lavoro pianificato. |
| name | `xsd:string` | Nome processo. |
| originalName | `xsd:string` | Nome originale del processo pianificato. |
| Testo | `xsd:string` | Tipo di processo. |
| submitUserEmail | `xsd:string` | L&#39;indirizzo e-mail dell&#39;utente che ha pianificato il processo. |
| locale | `xsd:string` | Impostazioni internazionali da utilizzare per i dettagli del registro di lavoro e la localizzazione delle e-mail. Le impostazioni internazionali sono specificate come `<language_code>[- <country_code>]`, se il codice della lingua è un codice a due lettere minuscolo, come specificato dalla norma ISO-639, e se il codice del paese opzionale è un codice a due lettere maiuscolo come specificato dalla norma ISO-3166. Ad esempio, la stringa locale per Inglese (Stati Uniti) è la seguente: `en-US`. |
| descrizione | `xsd:string` | Una descrizione del processo come specificato originariamente in `submitJob`. |
| execSchedule | `xsd:string` | Quando è pianificato l&#39;esecuzione del processo. |
| nextFireTime | `xsd:dateTime` | Data, ora e fuso orario in cui viene attivato il processo. |
| timeZone | `xsd:dateTime` | Fuso orario del processo pianificato. |
| triggerState | `xsd:int` | Scelta dello stato di attivazione del processo. |
| imageServingPublishJob | `types:ImageServingPublishJob` | Dettagli del processo per un processo di pubblicazione di image serving. |
| imageServingRenderJob | `types:ImageServingRenderJob` | Dettagli del processo per un processo di rendering delle immagini. |
| videoPublishJob | `types:VideoPublishJob` | Dettagli del processo per un processo di pubblicazione video. Vedi [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | Dettagli del processo per un processo di pubblicazione della directory del server. |
| uploadDirectoryJob | `types:UploadDirectoryJob` | Dettagli del processo per un processo della directory di caricamento. |
| uploadUrlsJob | `types:UploadUrlsJob` | Dettagli del processo per un processo di caricamento degli URL. |
| optimizeImagesJob | `types:OptimizeImagesJob` |  |
| ripPdfsJob | `types:RipPdfsJob` |  |
| reprocessAssetsJob | `types:ReprocessAssetsJob` |  |
| exportJob | `types:ExportJob` | Consenti esportazione autorizzata di file caricati in precedenza. Vedi [Processo di esportazione](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Note {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Quando si specifica un valore del tipo di processo in `submitJob`, il sistema restituisce un processo in base a quel tipo. È possibile restituire i seguenti lavori:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
