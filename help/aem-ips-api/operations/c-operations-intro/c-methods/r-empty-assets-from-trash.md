---
description: Svuota le risorse dal cestino IPS.
solution: Experience Manager
title: emptyAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 7%

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

Svuota le risorse dal cestino IPS.

Le risorse vivono nel cestino fino a quando non vengono svuotate manualmente o fino a quando non esauriscono il cestino. Se vengono svuotati manualmente, vivono nel Cestino fino al successivo lavoro di pulizia (normalmente notturno) quando vengono infine eliminati dal sistema. Se scadono dal cestino, le risorse vengono eliminate come parte della stessa attività di pulizia. Il timeout è configurabile (il valore predefinito è 7 giorni).

## Tipi di utenti autorizzati {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## Parametri {#section-8e1fb0ee3aae453581e99ef76e298569}

**Input (emptyAssetsFromTrashParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle dell’azienda proprietaria delle risorse. |
| `*`assetHandleArray`*` | `types:HandleArray` | Sì | Matrice di maniglie che rappresentano gli elementi da svuotare dal cestino. |

**Output (emptyAssetsFromTrashParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`successCount`*` | `xsd:Int` | Sì | Numero di risorse svuotate dal cestino. |
| `*`warningCount`*` | `xsd:Int` | Sì | Numero di avvisi generati quando l’operazione tentava di svuotare le risorse dal cestino. |
| `*`errorCount`*` | `xsd:Int` | Sì | Il numero di errori generati quando l&#39;operazione tentava di svuotare le risorse dal cestino. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato avvisi quando l’operazione tentava di svuotarle dal cestino. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato errori quando l’operazione tentava di svuotarle dal cestino. |

## Esempi {#section-6154a873b6c342bf92e2036280cafdcf}

Questo esempio di codice utilizza l’handle dell’azienda e una matrice di handle di risorsa che contiene gli handle per le risorse da svuotare dal cestino.

**Request Contents (Richiesta contenuto)**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Risposta**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```

