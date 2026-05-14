---
description: Elimina un tipo di insieme di proprietà e il relativo insieme di proprietà associato e le proprietà.
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
TQID: 'https://experienceleague.adobe.com/MslFY4FLpUm0zZRKTL6ZK4-seRyEMbF55r1LRToIFQY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 93
ht-degree: 5%

---

# deletePropertySetType{#deletepropertysettype}

Elimina un tipo di insieme di proprietà e il relativo insieme di proprietà associato e le proprietà.

Sintassi

## Tipi di utenti autorizzati {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-1c8973f5d35f44b4a6a483a41609e455}

**Input (deletePropertySetTypeParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| typeHandle | `xsd:string` | Sì | Handle del tipo di set di proprietà da eliminare. |

**Output (deletePropertySetTypeParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-85faa2e3411a4e23aa6489037f7ce078}

In questo esempio di codice viene utilizzato l&#39;handle del tipo come campo in `deletePropertySetTypeParam` inviato al server dei servizi Web IPS per eliminare il tipo del set di proprietà.

**Richiesta**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Risposta**

Nessuno.
