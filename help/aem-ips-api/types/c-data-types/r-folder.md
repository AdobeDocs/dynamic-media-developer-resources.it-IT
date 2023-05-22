---
description: File gerarchico o oggetto di archiviazione risorse. Le cartelle possono contenere una o più sottocartelle.
solution: Experience Manager
title: Cartella
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '70'
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
