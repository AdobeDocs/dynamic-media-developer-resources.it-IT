---
description: File gerarchico o oggetto di archiviazione risorse. Le cartelle possono contenere una o più sottocartelle.
solution: Experience Manager
title: Cartella
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
TQID: 'https://experienceleague.adobe.com/nh6zqOnt-bxAFmsHSHPRCMThKlOwi-9b9fep6ujKZyE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 5%

---

# [!DNL Folder]{#folder}

File gerarchico o oggetto di archiviazione risorse. Le cartelle possono contenere una o più sottocartelle.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| folderHandle | `xsd:string` | Handle di cartella. |
| [!DNL path] | `xsd:string` | Percorso cartella. |
| lastModified | `xsd:dateTime` | Data ultima modifica. |
| childLastModified | `xsd:dateTime` | Data dell’ultima modifica per le sottocartelle e le risorse secondarie delle cartelle. |
| permissionsSetHandle | `xsd:string` | Handle di autorizzazioni della cartella. |
| hasSubfolder | `types:Boolean` | Determina se una cartella contiene sottocartelle. |
| subfolderArray | `types:FolderArray` | Matrice di sottocartelle in una cartella. |
