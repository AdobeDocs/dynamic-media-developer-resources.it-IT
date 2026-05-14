---
description: Restituisce la cronologia di pubblicazione di una risorsa.
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
TQID: 'https://experienceleague.adobe.com/fXYa2SsttVpR9a1bebJ1oouyK8peSZ5GdgldPqU9s1g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 12%

---

# getAssetPublishHistory{#getassetpublishhistory}

Restituisce la cronologia di pubblicazione di una risorsa.

Sintassi

## Tipi di utenti autorizzati {#section-3b9d6a129093458fa8890139a2718912}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-3541bd9914a44b89acfc1d419b560ee6}

**Input (getAssetPublishHistoryParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle per l’azienda con la cronologia di pubblicazione delle risorse. |
| assetHandle | `xsd:string` | Sì | La risorsa con la cronologia di pubblicazione che desideri esaminare. |

**Output (getAssetPublishHistoryReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| pubHistoryArray | `types:PublishHistoryArray` | Sì | Cronologia di pubblicazione della risorsa. |

## Esempi {#section-53897c51e5a047c5bd5ea5a6efb2d114}

In questo esempio di codice viene restituita la cronologia di pubblicazione di una risorsa. Una risorsa non è mai stata pubblicata se il server restituisce un array vuoto.

**Richiesta**

```java
<getAssetPublishHistoryParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetPublishHistoryParam>
```

**Risposta**

```java
<getAssetPublishHistoryReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <pubHistoryArray/>
</getAssetPublishHistoryReturn>
```
