---
description: Sposta una risorsa in una cartella specifica.
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 12%

---


# moveAsset{#moveasset}

Sposta una risorsa in una cartella specifica.

Sintassi

## Tipi di utenti autorizzati {#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-dd0bbdf293aa4563af70a91f97c861f1}

**Input (moveAssetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Manda all&#39;azienda. |
| `*`assetHandle`*` | `xsd:string` | Sì | Gestisci la risorsa da spostare. |
| `*`folderHandle`*` | `xsd:string` | Sì | Gestisci la cartella di destinazione. |

**Output (moveAssetReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-78333769f4f14e2886fdf06433c9d2ad}

Questo codice di esempio sposta una risorsa in una cartella.

**Request Contents (Richiesta contenuto)**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**Risposta**

Nessuno.
