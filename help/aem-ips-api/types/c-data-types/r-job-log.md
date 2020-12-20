---
description: Registro dei processi dopo l’esecuzione del processo.
seo-description: Registro dei processi dopo l’esecuzione del processo.
seo-title: JobLog
solution: Experience Manager
title: JobLog
topic: Scene7 Image Production System API
uuid: d267009a-e4ad-4a21-ae0e-caf51d2f338b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 3%

---


# JobLog{#joblog}

Registro dei processi dopo l’esecuzione del processo.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Maniglia aziendale. |
| ` *`jobHandle`*` | `xsd:string` | Handle processo. |
| ` *`jobName`*` | `xsd:string` | Nome processo. |
| ` *`OriginalJobName`*` | `xsd:string` | Nome originale inviato per il processo con `submitJob`. |
| ` *`submitUserEmail`*` | `xsd:string` | L’indirizzo e-mail dell’utente che ha inviato il processo. |
| ` *`logType`*` | `xsd:string` | Scelta dei tipi di registro dei processi. |
| ` *`jobSubType`*` | `xsd:string` | Informazioni aggiuntive sul processo. |
| ` *`startDate`*` | `xsd:dateTime` | Data, ora e fuso orario di inizio del processo. |
| ` *`endDate`*` | `xsd:dateTime` | Data, ora e fuso orario di fine del processo. |
| ` *`description`*` | `xsd:string` | Una descrizione del processo come specificato originariamente in `submitJob`. |
| ` *`fileSuccessCount`*` | `xsd:int` | Numero di file elaborati correttamente. |
| ` *`fileErrorCount`*` | `xsd:int` | Numero di file che hanno causato un errore. |
| ` *`fileWarningCount`*` | `xsd:int` | Numero di file che hanno generato un avviso. |
| ` *`fileDuplicateCount`*` | `xsd:int` | Numero di file duplicati. |
| ` *`fileUpdateCount`*` | `xsd:int` | Numero di file aggiornati. |
| ` *`totalFileCount`*` | `xsd:int` | Numero di file elaborati dal processo registrato. |
| ` *`transferSuccessCount`*` | `xsd:int` | Numero di trasferimenti riusciti. |
| ` *`transferErrorCount`*` | `xsd:int` | Numero di errori di trasferimento. |
| ` *`transferWarningCount`*` | `xsd:int` | Numero di avvisi di trasferimento. |
| ` *`fatalError`*` | `xsd:boolean` | Se il processo ha generato un errore irreversibile. |
| ` *`detailTotalRows`*` | `xsd:int` | Il numero totale di righe corrispondenti alla query, che può essere maggiore della dimensione di `detailArray` a causa dei limiti di dimensione della pagina. |
| ` *`detailArray`*` | `types:JobLogDetailArray` | Array di dettagli sul processo registrato. |

