---
description: Restituisce la cronologia di pubblicazione di una risorsa.
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Developer,Administrator
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 14%

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
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle dell’azienda con la cronologia di pubblicazione delle risorse. |
| `*`assetHandle`*` | `xsd:string` | Sì | La risorsa con la cronologia di pubblicazione da esaminare. |

**Output (getAssetPublishHistoryReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`pubHistoryArray`*` | `types:PublishHistoryArray` | Sì | La cronologia di pubblicazione della risorsa. |

## Esempi {#section-53897c51e5a047c5bd5ea5a6efb2d114}

Questo esempio di codice restituisce la cronologia di pubblicazione di una risorsa. Una risorsa non è mai stata pubblicata se il server restituisce una matrice vuota.

**Request Contents (Richiesta contenuto)**

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
