---
description: Aggiorna un set di risorse.
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: af7899c4-a95f-42c8-858e-ed1592c6f5b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 18%

---

# updateAssetSet{#updateassetset}

Aggiorna un set di risorse.

Sintassi

## Parametri {#section-d7080ccd97334c94860eb107a3e132b2}

**Input (updateAssetSetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda contenente il set di immagini che si desidera modificare. |
| assetHandle | `xsd:string` | Sì | Handle del set di immagini da modificare. |
| setDefinition | `xsd:string` | No | Reimposta i membri del set di immagini. |
| thumbAssetHandle | `xsd:string` | No | Handle della risorsa che funge da miniatura per il set di immagini. |

**Output (updateAssetSetReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
|  |  |  |  |

## Esempi {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Request Contents (Richiesta contenuto)**

```java
<updateAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|535</assetHandle> 
  <setDefinition>${getCatalogId([a|202])};${getCatalogId([a|202])};advanced_image;,${getCatalogId([a|935])};${getCatalogId([a|935])};advanced_image;,${getCatalogId([a|933])};${getCatalogId([a|933])};advanced_image;</setDefinition> 
  <thumbAssetHandle>a|202</thumbAssetHandle> 
</updateAssetSetParam>
```

**Risposta**

```java
<updateAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```
