---
description: Ottiene le stringhe di ricerca, le parole chiave e altre informazioni su una risorsa. La risposta contiene informazioni aggiuntive sulla risorsa.
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
TQID: 'https://experienceleague.adobe.com/5w3SvwJWT7831IVQKCbpy7Tc-zULMfiva8UBuglcX-g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 95
ht-degree: 11%

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
| companyHandle | `xsd:string` | Sì | Gestire l&#39;azienda. |
| assetHandle | `xsd:string` | Sì | Gestisci la risorsa. |

**Output (getSearchStringsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| searchStringArray | `types:SearchStrings` | Sì | Matrice di stringhe per la ricerca di risorse. |

## Esempi {#section-e1f73bff6e4440c489d59cb9aa5384d8}

In questo esempio di codice vengono restituite stringhe di ricerca specifiche per la risorsa. La risposta restituisce un array vuoto.

**Richiesta**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Risposta**

Nessuno.
