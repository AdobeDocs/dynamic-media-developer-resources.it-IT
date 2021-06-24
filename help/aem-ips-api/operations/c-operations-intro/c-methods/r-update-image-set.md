---
description: Aggiorna un set di immagini.
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic, SDK/API, Set di immagini
role: Developer,Administrator
exl-id: d8d5fb80-17f1-424f-8a61-27189f87d603
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 16%

---

# updateImageSet{#updateimageset}

Aggiorna un set di immagini.

Sintassi

## Parametri {#section-3be47dbbce474ce78676b05e163492e3}

**Input (updateImageSetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società che contiene il set di immagini che desideri modificare. |
| `*`assetHandle`*` | `xsd:string` | Sì | La maniglia del set di immagini che si desidera modificare. |
| `*`MemberArray`*` | `types:ImageSetMemberUpdateArray` | No | Ripristina i membri del set di immagini. |
| `*`thumbAssetHandle`*` | `xsd:string` | No | La maniglia della risorsa che agisce come miniatura del set di immagini. |

**Output (updateImageSetReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`sequenza`*` |  |  |  |

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
