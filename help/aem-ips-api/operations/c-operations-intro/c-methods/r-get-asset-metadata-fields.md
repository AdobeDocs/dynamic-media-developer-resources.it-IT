---
description: Restituisce tutti i campi di metadati, raggruppati per tipo di risorsa.
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 20%

---

# getAssetMetadataFields{#getassetmetadatafields}

Restituisce tutti i campi di metadati, raggruppati per tipo di risorsa.

Sintassi

## Tipi di utenti autorizzati {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**Input (getAssetMetadataFieldsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | L&#39;handle dell&#39;azienda di cui si desidera recuperare i metadati. |

**Output (getAssetMetadataFieldsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| assetFieldArray | `types:AssetMetadataFieldsArray` | Sì | Array di campi di metadati, per tipo di risorsa. |

## Esempi {#section-d79ab85f29144635b0b61416e52f4f3f}

**Request Contents (Richiesta contenuto)**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**Risposta**

>[!NOTE]
>
>Troncato per brevità.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
