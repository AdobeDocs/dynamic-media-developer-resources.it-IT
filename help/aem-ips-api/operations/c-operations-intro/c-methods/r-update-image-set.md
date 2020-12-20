---
description: Aggiorna un set di immagini.
seo-description: Aggiorna un set di immagini.
seo-title: updateImageSet
solution: Experience Manager
title: updateImageSet
topic: Scene7 Image Production System API
uuid: df118ba3-d86f-4005-928e-76a5a9f899fc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 16%

---


# updateImageSet{#updateimageset}

Aggiorna un set di immagini.

Sintassi

## Parametri {#section-3be47dbbce474ce78676b05e163492e3}

**Input (updateImageSetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società che contiene il set di immagini da modificare. |
| ` *`assetHandle`*` | `xsd:string` | Ys | La maniglia del set di immagini da modificare. |
| ` *`MemberArray`*` | `types:ImageSetMemberUpdateArray` | No | Ripristina i membri del set di immagini. |
| ` *`thumbAssetHandle`*` | `xsd:string` | No | La maniglia della risorsa che funge da miniatura per il set di immagini. |

**Output (updateImageSetReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`sequence`*` |  |  |  |

## Esempi {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Request Contents (Richiesta contenuto)**

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**Risposta**

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

