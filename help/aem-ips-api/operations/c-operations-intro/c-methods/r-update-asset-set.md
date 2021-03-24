---
description: Aggiorna un set di risorse.
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 17%

---


# updateAssetSet{#updateassetset}

Aggiorna un set di risorse.

Sintassi

## Parametri {#section-d7080ccd97334c94860eb107a3e132b2}

**Input (updateAssetSetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società che contiene il set di immagini che desideri modificare. |
| `*`assetHandle`*` | `xsd:string` | Sì | La maniglia del set di immagini che si desidera modificare. |
| `*`setDefinition`*` | `xsd:string` | No | Ripristina i membri del set di immagini. |
| `*`thumbAssetHandle`*` | `xsd:string` | No | La maniglia della risorsa che agisce come miniatura del set di immagini. |

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

