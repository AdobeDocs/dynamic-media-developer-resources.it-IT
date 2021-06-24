---
description: Ottiene le stringhe di ricerca, le parole chiave e altre informazioni su una risorsa. La risposta contiene informazioni aggiuntive sulla risorsa.
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 15%

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
| `*`companyHandle`*` | `xsd:string` | Sì | Manda all&#39;azienda. |
| `*`assetHandle`*` | `xsd:string` | Sì | Gestisci la risorsa. |

**Output (getSearchStringsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`searchStringArray`*` | `types:SearchStrings` | Sì | Matrice di stringhe di ricerca delle risorse. |

## Esempi {#section-e1f73bff6e4440c489d59cb9aa5384d8}

Questo esempio di codice restituisce stringhe di ricerca specifiche per le risorse. La risposta restituisce una matrice vuota.

**Request Contents (Richiesta contenuto)**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Risposta**

Nessuno.
