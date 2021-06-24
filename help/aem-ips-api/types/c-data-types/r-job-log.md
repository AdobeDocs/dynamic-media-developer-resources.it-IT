---
description: Registro dei processi dopo l'esecuzione del processo.
solution: Experience Manager
title: Registro processi
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 3%

---

# Registro processi{#joblog}

Registro dei processi dopo l&#39;esecuzione del processo.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Tratta l&#39;azienda. |
| `*`jobHandle`*` | `xsd:string` | Maniglia di lavoro. |
| `*`jobName`*` | `xsd:string` | Nome processo. |
| `*`originalJobName`*` | `xsd:string` | Nome originale inviato per il processo con `submitJob`. |
| `*`submitUserEmail`*` | `xsd:string` | L’indirizzo e-mail dell’utente che ha inviato il processo. |
| `*`logType`*` | `xsd:string` | Scelta dei tipi di registro processi. |
| `*`jobSubType`*` | `xsd:string` | Informazioni aggiuntive sul processo. |
| `*`startDate`*` | `xsd:dateTime` | Data, ora e fuso orario di inizio del processo. |
| `*`endDate`*` | `xsd:dateTime` | Data, ora e fuso orario di fine del processo. |
| `*`descrizione`*` | `xsd:string` | Una descrizione del processo come specificato originariamente in `submitJob`. |
| `*`fileSuccessCount`*` | `xsd:int` | Numero di file elaborati correttamente. |
| `*`fileErrorCount`*` | `xsd:int` | Numero di file che hanno causato un errore. |
| `*`fileWarningCount`*` | `xsd:int` | Numero di file che hanno generato un avviso. |
| `*`fileDuplicateCount`*` | `xsd:int` | Numero di file duplicati. |
| `*`fileUpdateCount`*` | `xsd:int` | Numero di file aggiornati. |
| `*`totalFileCount`*` | `xsd:int` | Numero di file elaborati dal processo registrato. |
| `*`transferSuccessCount`*` | `xsd:int` | Numero di trasferimenti riusciti. |
| `*`transferErrorCount`*` | `xsd:int` | Numero di errori di trasferimento. |
| `*`transferWarningCount`*` | `xsd:int` | Numero di avvisi di trasferimento. |
| `*`fatalError`*` | `xsd:boolean` | Se il processo ha generato un errore irreversibile. |
| `*`detailTotalRows`*` | `xsd:int` | Il numero totale di righe che corrispondono alla query, che può essere maggiore della dimensione di `detailArray` a causa dei limiti di dimensione della pagina. |
| `*`detailArray`*` | `types:JobLogDetailArray` | Matrice di dettagli sul processo registrato. |
