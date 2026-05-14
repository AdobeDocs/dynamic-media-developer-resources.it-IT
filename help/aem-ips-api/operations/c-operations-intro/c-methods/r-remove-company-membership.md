---
description: Rimuove un utente da una o più società.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
TQID: 'https://experienceleague.adobe.com/5jjL8MnUtL046oSej3HErZB9hrD-ueEBC5-h9vD92HM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 6%

---

# removeCompanyMembership{#removecompanymembership}

Rimuove un utente da una o più società.

Sintassi

## Tipi di utenti autorizzati {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-6dfce5e44d8a4799afd0c231a0b10463}

**Input (removeCompanyMembershipParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| userHandle | `xsd:string` | No | Handle per l&#39;utente con l&#39;appartenenza che si desidera rimuovere. |
| companyHandleArray | `types:HandleArray` | Sì | Handle dell&#39;azienda da cui si sta rimuovendo l&#39;utente. |

**Output (removeCompanyMembershipReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-6b7903195e8647a1bd0502f87387ca62}

Questo esempio di codice rimuove un utente da un’azienda. Ometti l’handle utente facoltativo per rimuovere tutti gli utenti dalle aziende specificate nell’array dell’handle aziendale.

**Richiesta**

```java
<ns1:removeCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:removeCompanyMembershipParam>
```

**Risposta**

Nessuno.
