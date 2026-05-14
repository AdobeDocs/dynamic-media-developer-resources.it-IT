---
description: Elimina un set di proprietà e tutte le proprietà associate.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
TQID: 'https://experienceleague.adobe.com/1j45J5Kw5P-3ba3WLNy9sTDBC5g4L17bynJQRaU5lAM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 6%

---

# deletePropertySet{#deletepropertyset}

Elimina un set di proprietà e tutte le proprietà associate.

Sintassi

## Tipi di utenti autorizzati {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-e5fc868f69494cf6858e03027db09101}

**Input (deletePropertySetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| setHandle | `xsd:string` | Sì | Handle della proprietà impostata per l&#39;eliminazione. |

**Output (deletePropertySetParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-cf319fc8f86a40ab9cbd838b031973fe}

In questo esempio di codice viene utilizzato l&#39;handle del set come campo in `deletePropertySetParam` inviato al server dei servizi Web IPS per eliminare il set di proprietà.

**Richiesta**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Risposta**

Nessuno.
