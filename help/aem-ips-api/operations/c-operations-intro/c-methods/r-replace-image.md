---
description: Sostituisce i dati immagine per una risorsa immagine.
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
TQID: 'https://experienceleague.adobe.com/11bWPLId2s4gOVhiIFr93Ca4D-7SJ0PYHFmiSKtStjk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 11%

---

# replaceImage{#replaceimage}

Sostituisce i dati immagine per una risorsa immagine.

Sintassi

## Tipi di utenti autorizzati {#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**Input (replaceImageParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyName | `xsd:string` | Sì | Handle dell&#39;azienda con l&#39;immagine che si desidera sostituire. |
| assetHandle | `xsd:string` | Sì | Handle della risorsa da sostituire. |
| urlModifier | `xsd:string` | Sì | Comandi del server immagini che generano nuovi dati immagine. |

**Output (replaceImageReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| assetHandle | `xsd:string` | Sì | Gestisci la nuova risorsa. |

## Esempi {#section-cebb93576bde4cb98cb27356ca66783b}

Questo esempio di codice sostituisce un&#39;immagine e applica un `urlModifier` con un comando che specifica che il server immagini non esegue alcuna azione al momento della sostituzione.

**Richiesta**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**Risposta**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```
