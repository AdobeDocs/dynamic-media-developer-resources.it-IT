---
description: Imposta le autorizzazioni della cartella.
seo-description: Imposta le autorizzazioni della cartella.
seo-title: setFolderPermissions
solution: Experience Manager
title: setFolderPermissions
topic: Scene7 Image Production System API
uuid: 3a33034e-df2c-48ab-8ade-b76bea444388
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 12%

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
| ` *`companyHandle`*` | `xsd:string` | Sì | Maniglia aziendale. |
| ` *`folderHandle`*` | `xsd:string` | Sì | handle della cartella. |
| ` *`setChildren`*` | `xsd:boolean` | Sì | Imposta le autorizzazioni per gli elementi secondari che appartengono alla cartella. |
| ` *`permissionsArray`*` | `types:PermissionUpdateArray` | Sì | Matrice delle autorizzazioni. |

**Output (setFolderPermissionsReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-01730da4be874553ab44e3241cdf6357}

Questo esempio di codice specifica un handle della società, un handle di cartella e un array di autorizzazioni con informazioni dettagliate sulla cartella. Applica le stesse autorizzazioni per gli elementi secondari della cartella principale.

**Request Contents (Richiesta contenuto)**

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
