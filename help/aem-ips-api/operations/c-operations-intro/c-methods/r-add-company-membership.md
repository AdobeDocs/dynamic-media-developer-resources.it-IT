---
description: Aggiunge un utente a una o più società.
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 11%

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
| `*`userHandle`*` | `xsd:string` | No | L&#39;handle dell&#39;utente di cui si desidera aggiungere l&#39;iscrizione. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sì | Un array di aziende a cui aggiungere l’utente. |

**Output (addCompanyMembershipReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-5469f88bac7047cca131faa6b021e437}

In questo esempio viene utilizzato `*`companyHandleArray`*` per aggiungere un utente a una singola azienda.

**Request Contents (Richiesta contenuto)**

```java
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**Risposta**

Nessuno.
