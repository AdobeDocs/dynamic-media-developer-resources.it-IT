---
description: Imposta le autorizzazioni della cartella.
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 8%

---

# setFolderPermissions{#setfolderpermissions}

Imposta le autorizzazioni della cartella.

Sintassi

## Tipi di utenti autorizzati {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-2a41135054954396b40f1228f2e63b42}

**Input (setFolderPermissionsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Gestore azienda. |
| folderHandle | `xsd:string` | Sì | Handle di cartella. |
| setChildren | `xsd:boolean` | Sì | Imposta le autorizzazioni per gli elementi figlio che appartengono alla cartella. |
| permissionArray | `types:PermissionUpdateArray` | Sì | Array di autorizzazioni. |

**Output (setFolderPermissionsReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-01730da4be874553ab44e3241cdf6357}

Questo esempio di codice specifica un handle di società, un handle di cartella e un array di autorizzazioni con informazioni dettagliate sulla cartella. Applica le stesse autorizzazioni per gli elementi figlio della cartella principale.

**Richiesta**

```java
<setFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <setChildren>true</setChildren>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setFolderPermissionsParam>
```

**Risposta**

Nessuno.
