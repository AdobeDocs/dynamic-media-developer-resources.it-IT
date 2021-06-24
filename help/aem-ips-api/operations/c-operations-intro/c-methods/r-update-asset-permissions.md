---
description: Aggiorna le autorizzazioni delle risorse.
solution: Experience Manager
title: updateAssetPermissons
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Developer,Administrator
exl-id: 12972a52-7b70-405c-9c73-e5ce6ab7dd9b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 18%

---

# updateAssetPermissons{#updateassetpermissons}

Aggiorna le autorizzazioni delle risorse.

Sintassi

## Tipi di utenti autorizzati {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-392cb3076cf84790a32fd913f2b111a3}

**Input (updateAssetPermissionsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Tratta l&#39;azienda. |
| `*`assetHandle`*` | `xsd:string` | Sì | Gestione risorse. |
| `*`updateArray`*` | `types:PermissionUpdateArray` | Sì | Autorizzazioni da applicare alla risorsa. |

**Output (updateAssetPermissionsReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-1b7b7dbfdab34c819a53f3d33004e1f9}

**Request Contents (Richiesta contenuto)**

```java
<ns1:updateAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>false</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateAssetPermissionsParam>
```

**Risposta**

Nessuno.
