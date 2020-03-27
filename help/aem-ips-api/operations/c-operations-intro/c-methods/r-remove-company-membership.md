---
description: Rimuove un utente da una o più società.
seo-description: Rimuove un utente da una o più società.
seo-title: removeCompanyMembership
solution: Experience Manager
title: removeCompanyMembership
topic: Scene7 Image Production System API
uuid: af57fde0-2297-41da-87bf-f063fc313264
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`userHandle`*` | `xsd:string` | No | L’handle dell’utente con l’iscrizione da rimuovere. |
| ` *`companyHandleArray`*` | `types:HandleArray` | Sì | L’handle della società da cui si sta rimuovendo l’utente. |

**Output (removeCompanyMembershipReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-6b7903195e8647a1bd0502f87387ca62}

Questo esempio di codice rimuove un utente da una società. Omettete l&#39;handle utente facoltativo per rimuovere tutti gli utenti dalle società specificate nell&#39;array handle della società.

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
