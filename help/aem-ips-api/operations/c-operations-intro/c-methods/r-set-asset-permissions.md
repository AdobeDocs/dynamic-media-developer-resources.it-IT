---
description: Imposta le autorizzazioni di una singola risorsa utilizzando una risorsa di autorizzazione.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
TQID: 'https://experienceleague.adobe.com/dd96ai2DgoCqZ1NR-2rixSHDEaBSgk6ioQIqmG-1RoE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 5%

---

# setAssetPermissions{#setassetpermissions}

Imposta le autorizzazioni di una singola risorsa utilizzando una risorsa di autorizzazione.

Per impostazione predefinita, Assets eredita le autorizzazioni della cartella principale. Una volta impostate le autorizzazioni su una risorsa, questa non eredita più le autorizzazioni del relativo elemento padre, a meno che non si chiami `removeAssetPermissions`.

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

**Richiesta**

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
