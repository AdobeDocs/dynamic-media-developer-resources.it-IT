---
description: Imposta l'appartenenza a un gruppo per un utente.
seo-description: Imposta l'appartenenza a un gruppo per un utente.
seo-title: setGroupMembership
solution: Experience Manager
title: setGroupMembership
uuid: 3285fab0-92e4-4b88-9a3c-88cbb97d48c9
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '110'
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
