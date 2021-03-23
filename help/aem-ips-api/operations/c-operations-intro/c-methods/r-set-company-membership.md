---
description: Imposta l’iscrizione di un utente in una o più società.
seo-description: Imposta l’iscrizione di un utente in una o più società.
seo-title: setCompanyMembership
solution: Experience Manager
title: setCompanyMembership
uuid: 34c9d457-bc2e-4186-8a8f-50388410640a
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 10%

---


# setCompanyMembership{#setcompanymembership}

Imposta l’iscrizione di un utente in una o più società.

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
| `*`userHandle`*` | `xsd:sting` | No | Maniglia utente. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sì | Array di aziende. |

**Output (setCompanyMembershipParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-862c0cc32ce0407ab248028e690a8386}

Questo codice di esempio aggiunge un utente a un&#39;azienda. Se necessario, specifica più società nell&#39;array di gestione aziendale.

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
