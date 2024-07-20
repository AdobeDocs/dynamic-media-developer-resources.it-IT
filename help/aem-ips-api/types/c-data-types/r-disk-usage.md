---
description: Statistiche dello spazio su disco per una risorsa o una cartella.
solution: Experience Manager
title: UtilizzoDisco
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 6%

---

# [!DNL DiskUsage]{#diskusage}

Statistiche dello spazio su disco per una risorsa o una cartella.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| companyHandle | `xsd:string` | Gestore azienda. |
| companyName | `xsd:string` | Nome dell’azienda. |
| imageCount | `xsd:int` | Numero di immagini memorizzate. |
| diskSpaceUsage | `xsd:long` | Totale lato file in kilobyte. |
| lastModified | `xsd:dateTime` | Data, ora e fuso orario dell&#39;ultima modifica apportata al tipo `DiskUsage`. |
