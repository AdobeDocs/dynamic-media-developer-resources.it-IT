---
description: Aggiunge un utente a una o più società.
seo-description: Aggiunge un utente a una o più società.
seo-title: addCompanyMembership
solution: Experience Manager
title: addCompanyMembership
topic: Scene7 Image Production System API
uuid: be55041c-fc4e-46e8-bd2c-81b5931406f5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`userHandle`*` | `xsd:string` | No | L’handle per l’utente di cui si desidera aggiungere l’iscrizione. |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sì | Un array di società a cui si sta aggiungendo l&#39;utente. |

**Output (addCompanyMembershipReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-5469f88bac7047cca131faa6b021e437}

In questo esempio viene utilizzato ` *`companyHandleArray`*` per aggiungere un utente a una singola società.

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
