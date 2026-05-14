---
description: Aggiorna un set di risorse.
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: af7899c4-a95f-42c8-858e-ed1592c6f5b6
TQID: 'https://experienceleague.adobe.com/D74n9esGrb36fQcp35KsbB2DNEuddDt4EaKTH4uLlek'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 77
ht-degree: 15%

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
|   |  |  |  |

## Esempi {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Richiesta**

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
