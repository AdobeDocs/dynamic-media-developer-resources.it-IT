---
description: Rinomina una cartella.
solution: Experience Manager
title: rinominaCartella
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Developer,Administrator
exl-id: 2d4f1059-8018-4efb-a1ec-8eb560b1a58f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 18%

---

# rinominaCartella{#renamefolder}

Rinomina una cartella.

Sintassi

## Tipi di utenti autorizzati {#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utente deve disporre dell’accesso in lettura e scrittura alla risorsa.

## Parametri {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**Input (rinominaFolderParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Gestisci l&#39;azienda con le cartelle che desideri rinominare. |
| `*`folderHandle`*` | `xsd:string` | Sì | Gestisci la cartella. |
| `*`folderName`*` | `xsd:string` | Sì | Nuovo nome della cartella. |

**Output (ridenominazioneCartellaReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Sì | Gestisci la cartella rinominata. |

## Esempi {#section-98bdd2f88d164f488676e90aba1dc864}

Questo codice di esempio rinomina una cartella.

**Request Contents (Richiesta contenuto)**

```java
<ns1:renameFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/PDF/</ns1:folderHandle>
   <ns1:folderName>My Newly Renamed PDF Folder</ns1:folderName>
</ns1:renameFolderParam>
```

**Risposta**

```java
<renameFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderHandle>MyCompany/My Newly Renamed PDF Folder/</folderHandle>
</renameFolderReturn>
```
