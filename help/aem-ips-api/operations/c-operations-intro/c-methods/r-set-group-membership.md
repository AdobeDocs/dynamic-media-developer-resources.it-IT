---
description: Imposta iscrizione al gruppo per un utente.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 7%

---

# setGroupMembership{#setgroupmembership}

Imposta iscrizione al gruppo per un utente.

Sintassi

## Tipi di utenti autorizzati {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Input (setGroupMembershipParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| Handle utente | `xsd:string` | No | Handle del utente di cui si desidera impostare il iscrizione al gruppo. |
| CompanyHandle | `xsd:string` | No | Maniglia aziendale. |
| GroupHandleArray | `types:HandleArray` | Sì | Array di handle per gruppi a cui appartiene il utente. |

**Output (setGroupMembershipReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-67b86d259df24938896fe19061845811}

Questo esempio di codice rende l&#39;utente membro di un gruppo. Aggiungi un utente a più gruppi con l&#39;array di handle di gruppo.

**Richiesta**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**Risposta**

Nessuno.
