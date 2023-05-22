---
description: Processo pianificato per l'esecuzione.
solution: Experience Manager
title: Processo pianificato
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 2%

---

# [!DNL ScheduledJob]{#scheduledjob}

Processo pianificato per l&#39;esecuzione.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| companyHandle | `xsd:string` | Gestore azienda. |
| jobHandle | `xsd:string` | Handle di processo pianificato. |
| nome | `xsd:string` | Nome processo. |
| originalName | `xsd:string` | Nome originale del processo pianificato. |
| tipo | `xsd:string` | Tipo di processo. |
| submitUserEmail | `xsd:string` | L’indirizzo e-mail dell’utente che ha pianificato il processo. |
| locale | `xsd:string` | Impostazioni locali da utilizzare per i dettagli del registro processi e per la localizzazione delle e-mail. Le impostazioni internazionali sono specificate come `<language_code>[- <country_code>]`, dove il codice della lingua è un codice a due lettere minuscole come specificato dallo standard ISO-639 e il codice facoltativo del paese è un codice a due lettere maiuscole come specificato dallo standard ISO-3166. Ad esempio, la stringa delle impostazioni internazionali per l&#39;inglese (Stati Uniti) sarà: `en-US`. |
| descrizione | `xsd:string` | Una descrizione del processo come originariamente specificato in `submitJob`. |
| execSchedule | `xsd:string` | Quando è pianificata l’esecuzione del processo. |
| nextFireTime | `xsd:dateTime` | La data, l&#39;ora e il fuso orario in cui il processo viene avviato. |
| fuso orario | `xsd:dateTime` | Il fuso orario del processo pianificato. |
| triggerState | `xsd:int` | Scelta dello stato di attivazione del processo. |
| imageServingPublishJob | `types:ImageServingPublishJob` | Dettagli di un processo di pubblicazione di image server. |
| imageServingRenderJob | `types:ImageServingRenderJob` | Dettagli di un processo di rendering di immagini. |
| videoPublishJob | `types:VideoPublishJob` | Dettagli di un processo di pubblicazione video. Consulta [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | Dettagli del processo per un processo di pubblicazione della directory del server. |
| uploadDirectoryJob | `types:UploadDirectoryJob` | Dettagli del processo per un processo di caricamento directory. |
| uploadUrlsJob | `types:UploadUrlsJob` | Dettagli di un processo di caricamento URL. |
| optimizeImagesJob | `types:OptimizeImagesJob` |  |
| ripPdfsJob | `types:RipPdfsJob` |  |
| reprocessAssetsJob | `types:ReprocessAssetsJob` |  |
| exportJob | `types:ExportJob` | Consente l’esportazione autorizzata di file caricati in precedenza. Consulta [Processo di esportazione](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Note {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Quando si specifica un valore di tipo di processo in `submitJob`, il sistema restituisce un processo in base a tale tipo. È possibile restituire i seguenti processi:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
