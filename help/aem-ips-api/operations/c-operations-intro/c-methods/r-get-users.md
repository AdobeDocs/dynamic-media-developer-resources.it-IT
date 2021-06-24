---
description: Ottiene una matrice di utenti come specificato dagli handle di ruolo azienda, gruppo e utente. Questa operazione consente di ordinare gli utenti restituiti e filtrare per carattere.
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 9%

---

# getUsers{#getusers}

Ottiene una matrice di utenti come specificato dagli handle di ruolo azienda, gruppo e utente. Questa operazione consente di ordinare gli utenti restituiti e filtrare per carattere.

## Tipi di utenti autorizzati {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`includeInactive`*` | `xsd:boolean` | No | Includi o escludi gli utenti inattivi. Gli utenti amministratori non IPS devono essere membri attivi di almeno una società per essere autorizzati a effettuare chiamate API. Se l&#39;utente non dispone di appartenenze attive alla società, verrà restituito un errore di autorizzazione. |
| `*`includeInvalid`*` | `xsd:boolean` | No | Consente di includere/escludere utenti non validi. |
| `*`companyHandleArray`*` | `types:HandleArray` | No | Filtrare i risultati per azienda. |
| `*`groupHandleArray`*` | `types:HandleArray` | No | Filtrare i risultati per gruppo. |
| `*`userRoleArray`*` | `types:StringArray` | No | Filtrare i risultati per ruolo utente. |
| `*`charFilterField`*` | `xsd:string` | No | Filtra i risultati per prefisso della stringa del campo (vedi [!DNL Trash State).] |
| `*`charFilter`*` | `xsd:string` | No | Filtrare i risultati per un carattere specifico. |
| `*`sortBy`*` | `xsd:string` | No | Scelta dei campi di ordinamento utente. |
| `*`recordsPerPage`*` | `xsd:int` | No | Restituisce il numero specificato di record per pagina. |
| `*`resultPage`*` | `xsd:int` | No | Pagina dei risultati. |

**Output (getUsersReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | Sì | Un array di utenti. |

## Esempi {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Questo esempio di codice restituisce l&#39;array di utenti per diversi parametri facoltativi. I ruoli utente, i campi filtro caratteri utente e i campi di ordinamento utente sono determinati utilizzando costanti stringa specifiche.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
   <ns1:userRoleArray>
      <ns1:items>IpsAdmin</ns1:items>
   </ns1:userRoleArray>
   <ns1:sortBy>LastName</ns1:sortBy>
</ns1:getUsersParam>
```

**Risposta**

```java
<getUsersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userArray>
      <items>
         <userHandle>70|kmagnusson@adobe.com</userHandle>
         <firstName>Kris</firstName>
         <lastName>Magnusson</lastName>
         <email>kmagnusson@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-27T15:18:15.816-07:00</passwordExpires>
      </items>
      ...
   </userArray>
</getUsersReturn>
```
