---
description: Imposta le autorizzazioni di una singola risorsa utilizzando una risorsa di autorizzazione.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 8%

---

# setAssetPermissions{#setassetpermissions}

Imposta le autorizzazioni di una singola risorsa utilizzando una risorsa di autorizzazione.

Per impostazione predefinita, le risorse ereditano le autorizzazioni della cartella principale. Una volta impostate le autorizzazioni su una risorsa, questa non eredita più le autorizzazioni del relativo elemento padre, a meno che tu non chiami `removeAssetPermissions`.

## Tipi di utenti autorizzati {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-e05abbce6453450fb38747101cb5e228}

**Input (setAssetPermissonsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda contenente la cartella che si desidera utilizzare. |
| assetHandle | `xsd:string` | Sì | Handle di cartella. |
| permissionArray | `types:PermissionsUpdateArray` | Sì | Array di autorizzazioni. |

**Output (setAssetPermissonsReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-38955bc330bb4909b6b06027ef2b143e}

Questo esempio di codice imposta le autorizzazioni per una risorsa. Contiene l’handle della società e della risorsa e un array di autorizzazioni.

**Request Contents (Richiesta contenuto)**

```java
<setAssetPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <assetHandle>97374|1|61046</assetHandle>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setAssetPermissionsParam>
```

**Risposta**

Nessuno.
