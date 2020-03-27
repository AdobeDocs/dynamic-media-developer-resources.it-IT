---
description: Ottiene gli utenti che appartengono a una società e a un gruppo specifici.
seo-description: Ottiene gli utenti che appartengono a una società e a un gruppo specifici.
seo-title: getGroupMembers
solution: Experience Manager
title: getGroupMembers
topic: Scene7 Image Production System API
uuid: 02322b66-1c0c-4d84-a3eb-97a4fb605318
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società. |
| ` *`groupHandle`*` | `xsd:string` |  | L&#39;handle del gruppo. |

**Output (getGroupMembersReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`userHandleArray`*` | `type:HandleArray` | Sì | Un array di handle utente. |

## Esempi {#section-aaa340dba6b64cce9bcd8303cf999166}

Questo esempio di codice restituisce un array di handle utente contenente tutti gli utenti appartenenti a un gruppo specifico.

**Request Contents (Richiesta contenuto)**

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

