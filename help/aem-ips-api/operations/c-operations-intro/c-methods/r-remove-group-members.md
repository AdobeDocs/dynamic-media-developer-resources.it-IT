---
description: Rimuove gli utenti aziendali da un gruppo specifico.
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 9%

---

# removeGroupMembers{#removegroupmembers}

Rimuove gli utenti aziendali da un gruppo specifico.

**Differenze tra i comandi Rimuovi**

* `removeGroupMembers`: Rimuove più utenti da un gruppo.
* `removeGroupMembership`: Rimuove un singolo utente da una matrice di gruppi.

## Tipi di utenti autorizzati {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-b5596614a3be4ce5962455884e4636af}

**Input (removeGroupMembersParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle dell’azienda con gli utenti con cui desideri lavorare. |
| `*`groupHandle`*` | `xsd:string` | Sì | Maniglia di gruppo. |
| `*`userHandleArray`*` | `types:HandleArray` | Sì | Matrice di handle per gli utenti di cui si desidera rimuovere le appartenenze al gruppo. |

**Output (removeGroupMembersParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-9eedac852cea46ec80de6a6928bf97ac}

Questo esempio di codice rimuove un utente dalla società specificata. Rimuovere più utenti da un gruppo con l&#39;array handle utente.

**Request Contents (Richiesta contenuto)**

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**Risposta**

Nessuno.
