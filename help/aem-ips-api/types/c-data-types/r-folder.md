---
description: Oggetto di memorizzazione gerarchica di file o risorse. Le cartelle possono contenere una (o più) sottocartelle.
seo-description: Oggetto di memorizzazione gerarchica di file o risorse. Le cartelle possono contenere una (o più) sottocartelle.
seo-title: Cartella
solution: Experience Manager
title: Cartella
topic: Scene7 Image Production System API
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Cartella{#folder}

Oggetto di memorizzazione gerarchica di file o risorse. Le cartelle possono contenere una (o più) sottocartelle.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | handle della cartella. |
| ` *`path`*` | `xsd:string` | Percorso cartella. |
| ` *`lastModified`*` | `xsd:dateTime` | Data ultima modifica. |
| ` *`childLastModified`*` | `xsd:dateTime` | Data ultima modifica per le sottocartelle e le risorse secondarie della cartella. |
| ` *`permissionsSetHandle`*` | `xsd:string` | Gestione delle autorizzazioni della cartella. |
| ` *`hasSubfolder`*` | `types:Boolean` | Determina se una cartella contiene sottocartelle. |
| ` *`subfolderArray`*` | `types:FolderArray` | Un array di sottocartelle in una cartella. |

