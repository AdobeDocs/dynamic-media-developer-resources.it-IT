---
description: Ottiene le stringhe di ricerca, le parole chiave e altre informazioni su una risorsa. La risposta contiene informazioni aggiuntive sulla risorsa.
seo-description: Ottiene le stringhe di ricerca, le parole chiave e altre informazioni su una risorsa. La risposta contiene informazioni aggiuntive sulla risorsa.
seo-title: getSearchStrings
solution: Experience Manager
title: getSearchStrings
topic: Scene7 Image Production System API
uuid: 9d588d6b-c79c-4531-a2e8-8467254a7985
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getSearchStrings{#getsearchstrings}

Ottiene le stringhe di ricerca, le parole chiave e altre informazioni su una risorsa. La risposta contiene informazioni aggiuntive sulla risorsa.

Sintassi

## Tipi di utenti autorizzati {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-c1efda4bb15349a68b276bafee8c18fd}

**Input (getSearchStringsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | Gestite l&#39;azienda. |
| ` *`assetHandle`*` | `xsd:string` | Sì | Consente di gestire la risorsa. |

**Output (getSearchStringsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`searchStringArray`*` | `types:SearchStrings` | Sì | Un array di stringhe di ricerca delle risorse. |

## Esempi {#section-e1f73bff6e4440c489d59cb9aa5384d8}

Questo esempio di codice restituisce stringhe di ricerca specifiche per le risorse. La risposta restituisce un array vuoto.

**Request Contents (Richiesta contenuto)**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Risposta**

Nessuno.
