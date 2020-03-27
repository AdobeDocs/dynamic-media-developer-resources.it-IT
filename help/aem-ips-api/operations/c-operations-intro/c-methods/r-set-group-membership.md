---
description: Imposta l’appartenenza a un gruppo per un utente.
seo-description: Imposta l’appartenenza a un gruppo per un utente.
seo-title: setGroupMembership
solution: Experience Manager
title: setGroupMembership
topic: Scene7 Image Production System API
uuid: 3285fab0-92e4-4b88-9a3c-88cbb97d48c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setGroupMembership{#setgroupmembership}

Imposta l’appartenenza a un gruppo per un utente.

Sintassi

## Tipi di utenti autorizzati {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Input (setGroupMembershipParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | No | L’handle per l’utente di cui si desidera impostare l’appartenenza al gruppo. |
| ` *`companyHandle`*` | `xsd:string` | No | Maniglia aziendale. |
| ` *`groupHandleArray`*` | `types:HandleArray` | Sì | L&#39;array di handle per i gruppi a cui l&#39;utente appartiene. |

**Output (setGroupMembershipReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-67b86d259df24938896fe19061845811}

Questo esempio di codice rende l’utente membro di un gruppo. Aggiungete un utente a più gruppi con l&#39;array delle maniglie del gruppo.

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
