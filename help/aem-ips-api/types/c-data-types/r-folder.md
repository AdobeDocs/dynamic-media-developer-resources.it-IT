---
description: Oggetto di archiviazione di file o risorse gerarchici. Le cartelle possono contenere una (o più) sottocartelle.
solution: Experience Manager
title: Cartella
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
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

