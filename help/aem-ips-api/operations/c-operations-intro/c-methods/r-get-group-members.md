---
description: Ottiene gli utenti che appartengono a una società e a un gruppo specifici.
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 12%

---

# getGroupMembers{#getgroupmembers}

Ottiene gli utenti che appartengono a una società e a un gruppo specifici.

Sintassi

## Tipi di utenti autorizzati {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-b798b06354c946abbb90fa72cc9c67fd}

**Input (getGroupMembersParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | La maniglia per l&#39;azienda. |
| groupHandle | `xsd:string` |  | Handle del gruppo. |

**Output (getGroupMembersReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| userHandleArray | `type:HandleArray` | Sì | Array di handle utente. |

## Esempi {#section-aaa340dba6b64cce9bcd8303cf999166}

In questo esempio di codice viene restituito un array di handle utente contenente tutti gli utenti che appartengono a un gruppo specifico.

**Richiesta**

```java
<ns1:getGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
</ns1:getGroupMembersParam>
```

**Risposta**

```java
<getGroupMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userHandleArray>
      <items>70|kmagnusson@adobe.com</items>
   </userHandleArray>
</getGroupMembersReturn>
```
