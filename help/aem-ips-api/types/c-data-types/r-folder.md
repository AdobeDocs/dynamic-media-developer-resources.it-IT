---
description: Oggetto di archiviazione di file o risorse gerarchici. Le cartelle possono contenere una (o più) sottocartelle.
solution: Experience Manager
title: Cartella
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 8%

---

# Cartella{#folder}

Oggetto di archiviazione di file o risorse gerarchici. Le cartelle possono contenere una (o più) sottocartelle.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| folderHandle | `xsd:string` | Maniglia della cartella. |
| path | `xsd:string` | Percorso cartella. |
| lastModified | `xsd:dateTime` | Data ultima modifica. |
| childLastModified | `xsd:dateTime` | Data ultima modifica per le sottocartelle e le risorse secondarie della cartella. |
| permissionsSetHandle | `xsd:string` | Gestione delle autorizzazioni della cartella. |
| hasSubfolder | `types:Boolean` | Determina se una cartella contiene sottocartelle. |
| subfolderArray | `types:FolderArray` | Matrice di sottocartelle in una cartella. |
