---
description: Elimina un gruppo.
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
TQID: 'https://experienceleague.adobe.com/skfJjk-dexrQR94ImWtaWV-1hkPmvrlFVn-EyA5mKtQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 6%

---

# deleteGroup{#deletegroup}

Elimina un gruppo.

Sintassi

## Tipi di utenti autorizzati {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-42775102ec724c36ae5241eea1a00b8e}

**Input (deleteGroupParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda appartenente al gruppo che si desidera eliminare. |
| groupHandle | `xsd:string` | Sì | Handle del gruppo che si desidera eliminare. |

**Output (deleteGroupParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Questo codice di esempio elimina un gruppo da un’azienda. Richiede un handle di gruppo che è necessario ottenere da un&#39;altra operazione.

**Richiesta**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Risposta**

Nessuno.
