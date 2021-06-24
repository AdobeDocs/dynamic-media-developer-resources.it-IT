---
description: Imposta l'appartenenza a un gruppo per un utente.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 10%

---

# setGroupMembership{#setgroupmembership}

Imposta l&#39;appartenenza a un gruppo per un utente.

Sintassi

## Tipi di utenti autorizzati {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Input (setGroupMembershipParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | No | L&#39;handle dell&#39;utente di cui si desidera impostare l&#39;appartenenza al gruppo. |
| `*`companyHandle`*` | `xsd:string` | No | Tratta l&#39;azienda. |
| `*`groupHandleArray`*` | `types:HandleArray` | Sì | Matrice di handle per i gruppi a cui appartiene l&#39;utente. |

**Output (setGroupMembershipReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-67b86d259df24938896fe19061845811}

Questo esempio di codice rende l&#39;utente un membro di un gruppo. Aggiungi un utente a più gruppi con l&#39;array di handle di gruppo.

**Request Contents (Richiesta contenuto)**

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
