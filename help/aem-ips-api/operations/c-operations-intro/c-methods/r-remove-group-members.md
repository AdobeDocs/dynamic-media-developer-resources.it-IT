---
description: Rimuove gli utenti della società da un gruppo specifico.
seo-description: Rimuove gli utenti della società da un gruppo specifico.
seo-title: removeGroupMembers
solution: Experience Manager
title: removeGroupMembers
topic: Dynamic Media Image Production System API
uuid: dd0ea335-bbd0-43b1-830b-77f32dc39b12
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 8%

---


# removeGroupMembers{#removegroupmembers}

Rimuove gli utenti della società da un gruppo specifico.

**Differenze tra i comandi Rimuovi**

* `removeGroupMembers`: Rimuove più utenti da un gruppo.
* `removeGroupMembership`: Rimuove un singolo utente da un array di gruppi.

## Tipi di utenti autorizzati {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-b5596614a3be4ce5962455884e4636af}

**Input (removeGroupMembersParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle della società con gli utenti con cui desiderate lavorare. |
| `*`groupHandle`*` | `xsd:string` | Sì | handle del gruppo. |
| `*`userHandleArray`*` | `types:HandleArray` | Sì | Un array di handle per gli utenti di cui si desidera rimuovere le appartenenze al gruppo. |

**Output (removeGroupMembersParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-9eedac852cea46ec80de6a6928bf97ac}

Questo esempio di codice rimuove un utente dalla società specificata. Rimuovete più utenti da un gruppo con l&#39;array di handle dell&#39;utente.

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
