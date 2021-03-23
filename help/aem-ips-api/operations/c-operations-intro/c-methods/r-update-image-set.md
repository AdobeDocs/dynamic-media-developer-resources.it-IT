---
description: Aggiorna un set di immagini.
seo-description: Aggiorna un set di immagini.
seo-title: updateImageSet
solution: Experience Manager
title: updateImageSet
uuid: df118ba3-d86f-4005-928e-76a5a9f899fc
feature: Dynamic Media Classic, SDK/API, Set di immagini
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 15%

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

