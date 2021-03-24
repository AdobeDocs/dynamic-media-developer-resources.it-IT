---
description: Rimuove le autorizzazioni dalle risorse selezionate.
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 12%

---


# removeAssetPermissions{#removeassetpermissions}

Rimuove le autorizzazioni dalle risorse selezionate.

Sintassi

## Tipi di utenti autorizzati {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**Input (removeAssetPermissionsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Il manico per l&#39;azienda. |
| `*`assetHandle`*` | `xsd:string` | Sì | L’handle della risorsa con le autorizzazioni da rimuovere. |

**Output (removeAssetPermissionsReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-238fa7bb091548f5ba72ced11fc92d4f}

Questo esempio di codice rimuove le autorizzazioni da una risorsa.

**Request Contents (Richiesta contenuto)**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**Risposta**

Nessuno.
