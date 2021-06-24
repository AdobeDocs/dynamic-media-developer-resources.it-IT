---
description: Aggiunge utenti da una società specifica a un gruppo specifico.
solution: Experience Manager
title: addGroupMembers
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: c03525e3-6bc4-4c6a-bb5b-b0cb2e6f6d0d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 10%

---

# addGroupMembers{#addgroupmembers}

Aggiunge utenti da una società specifica a un gruppo specifico.

Sintassi

## Tipi di utenti autorizzati {#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-b28434dcf2ca4b4ea431136aac33913e}

**Input (addGroupMembersParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Il manico per l&#39;azienda. |
| `*`groupHandle`*` | `xsd:string` | Sì | La maniglia del gruppo. |
| `*`userHandleArray`*` | `types:HandleArray` | Sì | Matrice di handle per gli utenti che si desidera aggiungere a un gruppo. |

**Output (addGroupMembersParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-8f168b528aef4c4fa8c3d41f7686842f}

In questo esempio viene utilizzato `*`addGroupMembersParam`*` per aggiungere un utente a una singola azienda. L&#39;API IPS non restituisce una risposta per questa operazione.

**Request Contents (Richiesta contenuto)**

```java
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**Risposta**

Nessuno.
