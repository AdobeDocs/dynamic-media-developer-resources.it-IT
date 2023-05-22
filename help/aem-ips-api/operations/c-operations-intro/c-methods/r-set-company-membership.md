---
description: Imposta l'appartenenza di un utente a una o più società.
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 11%

---

# setCompanyMembership{#setcompanymembership}

Imposta l&#39;appartenenza di un utente a una o più società.

Sintassi

## Tipi di utenti autorizzati {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-3930dc6a016140178631083563598104}

**Input (setCompanyMembershipParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| userHandle | `xsd:sting` | No | Handle utente. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Sì | Array di aziende. |

**Output (setCompanyMembershipParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-862c0cc32ce0407ab248028e690a8386}

Questo esempio di codice aggiunge un utente a un’azienda. Se necessario, specifica più aziende nell’array di handle della società.

**Request Contents (Richiesta contenuto)**

```java
<ns1:setCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>137</ns1:items>
   </ns1:companyHandleArray>
</ns1:setCompanyMembershipParam>
```

**Risposta**

Nessuno.
