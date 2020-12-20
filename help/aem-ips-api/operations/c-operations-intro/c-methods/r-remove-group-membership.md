---
description: Rimuove gli utenti da un array di gruppi.
seo-description: Rimuove gli utenti da un array di gruppi.
seo-title: removeGroupMembership
solution: Experience Manager
title: removeGroupMembership
topic: Scene7 Image Production System API
uuid: 553d91a3-73d6-4323-9436-a3ba13260a6c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 9%

---


# removeGroupMembership{#removegroupmembership}

Rimuove gli utenti da un array di gruppi.

**Differenze tra i comandi Rimuovi**

* `removeGroupMembers`: Rimuove più utenti da un gruppo.
* `removeGroupMembership`: Rimuove un singolo utente da un array di gruppi.

## Tipi di utenti autorizzati {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**Input (removeGroupMembershipParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | No | L’handle della società di cui si desidera rimuovere l’appartenenza al gruppo. |
| ` *`groupHandleArray`*` | `types:HandleArray` | Sì | L&#39;array di handle per i gruppi da cui si desidera rimuovere la società. |

**Output (removeGroupMembershipReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-f8d4181170a243efb9faf5824ae96197}

Questo esempio di codice rimuove un utente da un gruppo.

**Request Contents (Richiesta contenuto)**

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
