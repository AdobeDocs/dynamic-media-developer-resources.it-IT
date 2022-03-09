---
description: Aggiunge un utente a una o più società.
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 12%

---

# addCompanyMembership{#addcompanymembership}

Aggiunge un utente a una o più società.

Sintassi

## Tipi di utenti autorizzati {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**Input (addCompanyMembershipParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| userHandle | `xsd:string` | No | L&#39;handle dell&#39;utente di cui si desidera aggiungere l&#39;iscrizione. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Sì | Un array di aziende a cui aggiungere l’utente. |

**Output (addCompanyMembershipReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-5469f88bac7047cca131faa6b021e437}

In questo esempio viene utilizzato companyHandleArray per aggiungere un utente a una singola società.

**Request Contents (Richiesta contenuto)**

```javascript {.line-numbers}
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**Risposta**

Nessuno.
