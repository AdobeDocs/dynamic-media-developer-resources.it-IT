---
description: Rimuove gli utenti da un array di gruppi.
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 892ee01c-e07b-4321-b0b7-5bb606036340
TQID: 'https://experienceleague.adobe.com/-RTuwtlTpQdiS-H-lf9BhQwbkp5McXo4tbxssF-0wzo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 5%

---

# removeGroupMembership{#removegroupmembership}

Rimuove gli utenti da un array di gruppi.

**Differenze tra i comandi di rimozione**

* `removeGroupMembers`: rimuove più utenti da un gruppo.
* `removeGroupMembership`: rimuove un singolo utente da un array di gruppi.

## Tipi di utenti autorizzati {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Input (removeGroupMembershipParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| userHandle | `xsd:string` | No | Handle dell&#39;azienda di cui si desidera rimuovere l&#39;appartenenza al gruppo. |
| groupHandleArray | `types:HandleArray` | Sì | Array di handle ai gruppi da cui si desidera rimuovere la società. |

**Output (removeGroupMembershipReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-f8d4181170a243efb9faf5824ae96197}

Questo esempio di codice rimuove un utente da un gruppo.

**Richiesta**

```java
<ns1:removeGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>47</ns1:userHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:removeGroupMembershipParam>
```

**Risposta**

Nessuno.
