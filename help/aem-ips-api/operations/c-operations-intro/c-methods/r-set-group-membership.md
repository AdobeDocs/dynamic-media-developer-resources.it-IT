---
description: Imposta l'appartenenza al gruppo per un utente.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
TQID: 'https://experienceleague.adobe.com/j-wK2g-evSRY0YD3ZspgT--giCkKJl1VBYgPylixVz8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 7%

---

# setGroupMembership{#setgroupmembership}

Imposta l&#39;appartenenza al gruppo per un utente.

Sintassi

## Tipi di utenti autorizzati {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Input (setGroupMembershipParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| userHandle | `xsd:string` | No | Handle per l&#39;utente di cui si desidera impostare l&#39;appartenenza al gruppo. |
| companyHandle | `xsd:string` | No | Gestore azienda. |
| groupHandleArray | `types:HandleArray` | Sì | Array di handle ai gruppi a cui appartiene l&#39;utente. |

**Output (setGroupMembershipReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-67b86d259df24938896fe19061845811}

Questo esempio di codice rende l&#39;utente membro di un gruppo. Aggiungere un utente a più gruppi con l&#39;array dell&#39;handle di gruppo.

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
