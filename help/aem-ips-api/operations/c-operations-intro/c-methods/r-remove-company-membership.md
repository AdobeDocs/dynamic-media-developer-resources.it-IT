---
description: Rimuove un utente da una o più società.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 9%

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

**Request Contents (Richiesta contenuto)**

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
