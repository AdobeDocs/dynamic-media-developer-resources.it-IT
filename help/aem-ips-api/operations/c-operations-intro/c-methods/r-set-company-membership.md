---
description: Imposta l'iscrizione di un utente in una o più società.
seo-description: Imposta l'iscrizione di un utente in una o più società.
seo-title: setCompanyMembership
solution: Experience Manager
title: setCompanyMembership
topic: Dynamic Media Image Production System API
uuid: 34c9d457-bc2e-4186-8a8f-50388410640a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 11%

---


# setCompanyMembership{#setcompanymembership}

Imposta l&#39;iscrizione di un utente in una o più società.

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
| `*`userHandle`*` | `xsd:sting` | No | handle utente. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sì | Array di società. |

**Output (setCompanyMembershipParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-862c0cc32ce0407ab248028e690a8386}

Questo esempio di codice aggiunge un utente a una società. Se necessario, specificate più società nell&#39;array di handle della società.

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
