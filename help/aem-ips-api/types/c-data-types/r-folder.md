---
description: Oggetto di archiviazione di file o risorse gerarchici. Le cartelle possono contenere una (o più) sottocartelle.
seo-description: Oggetto di archiviazione di file o risorse gerarchici. Le cartelle possono contenere una (o più) sottocartelle.
seo-title: Cartella
solution: Experience Manager
title: Cartella
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 7%

---


# Cartella{#folder}

Oggetto di archiviazione di file o risorse gerarchici. Le cartelle possono contenere una (o più) sottocartelle.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Maniglia della cartella. |
| `*`path`*` | `xsd:string` | Percorso cartella. |
| `*`lastModified`*` | `xsd:dateTime` | Data ultima modifica. |
| `*`childLastModified`*` | `xsd:dateTime` | Data ultima modifica per le sottocartelle e le risorse secondarie della cartella. |
| `*`permissionsSetHandle`*` | `xsd:string` | Gestione delle autorizzazioni della cartella. |
| `*`hasSubfolder`*` | `types:Boolean` | Determina se una cartella contiene sottocartelle. |
| `*`subfolderArray`*` | `types:FolderArray` | Matrice di sottocartelle in una cartella. |

