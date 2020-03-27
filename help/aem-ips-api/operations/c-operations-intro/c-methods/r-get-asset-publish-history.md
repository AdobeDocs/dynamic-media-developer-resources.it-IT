---
description: Restituisce la cronologia di pubblicazione di una risorsa.
seo-description: Restituisce la cronologia di pubblicazione di una risorsa.
seo-title: getAssetPublishHistory
solution: Experience Manager
title: getAssetPublishHistory
topic: Scene7 Image Production System API
uuid: 15025c3d-eac3-4cb8-9a2a-fd80bd67478f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società con la cronologia di pubblicazione della risorsa. |
| ` *`assetHandle`*` | `xsd:string` | Sì | La risorsa con la cronologia di pubblicazione da esaminare. |

**Output (getAssetPublishHistoryReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`pubHistoryArray`*` | `types:PublishHistoryArray` | Sì | Cronologia di pubblicazione della risorsa. |

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

