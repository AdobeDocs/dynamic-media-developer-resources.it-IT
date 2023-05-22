---
description: Registro del processo dopo l'esecuzione del processo.
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# [!DNL JobLog]{#joblog}

Registro del processo dopo l&#39;esecuzione del processo.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| companyHandle | `xsd:string` | Gestore azienda. |
| jobHandle | `xsd:string` | Handle di processo. |
| jobName | `xsd:string` | Nome processo. |
| originalJobName | `xsd:string` | Nome originale inviato per il processo con `submitJob`. |
| submitUserEmail | `xsd:string` | L’indirizzo e-mail dell’utente che ha inviato il processo. |
| logType | `xsd:string` | Scelta dei tipi di registro processo. |
| jobSubType | `xsd:string` | Informazioni aggiuntive sul processo. |
| startDate | `xsd:dateTime` | La data di inizio, l&#39;ora e il fuso orario del processo. |
| endDate | `xsd:dateTime` | La data di fine, l&#39;ora e il fuso orario del processo. |
| [!DNL description] | `xsd:string` | Una descrizione del processo come originariamente specificato in `submitJob`. |
| fileSuccessCount | `xsd:int` | Numero di file elaborati correttamente. |
| fileErrorCount | `xsd:int` | Numero di file che hanno causato un errore. |
| fileWarningCount | `xsd:int` | Numero di file che hanno generato un avviso. |
| fileDuplicateCount | `xsd:int` | Numero di file duplicati. |
| fileUpdateCount | `xsd:int` | Numero di file aggiornati. |
| totalFileCount | `xsd:int` | Numero di file elaborati dal processo registrato. |
| transferSuccessCount | `xsd:int` | Numero di trasferimenti riusciti. |
| transferErrorCount | `xsd:int` | Numero di errori di trasferimento. |
| transferWarningCount | `xsd:int` | Numero di avvisi di trasferimento. |
| fatalError | `xsd:boolean` | Indica se il processo ha generato un errore irreversibile. |
| detailTotalRows | `xsd:int` | Numero totale di righe corrispondenti alla query, che può essere maggiore della dimensione di `detailArray` a causa dei limiti di dimensione delle pagine. |
| detailArray | `types:JobLogDetailArray` | Array di dettagli sul processo registrato. |
