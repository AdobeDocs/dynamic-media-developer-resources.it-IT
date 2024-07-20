---
description: Ottiene un array di utenti come specificato dagli handle di ruolo società, gruppo e utente. Questa operazione consente di ordinare gli utenti restituiti e filtrare per carattere.
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 9%

---

# getUsers{#getusers}

Ottiene un array di utenti come specificato dagli handle di ruolo società, gruppo e utente. Questa operazione consente di ordinare gli utenti restituiti e filtrare per carattere.

## Tipi di utenti autorizzati {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| includeInactive | `xsd:boolean` | No | Includere o escludere gli utenti inattivi. Per poter essere autorizzati a effettuare chiamate API, gli utenti non amministratori IPS devono essere membri attivi di almeno una società. Se l&#39;utente non dispone di appartenenze aziendali attive, viene restituito un errore di autorizzazione. |
| includeInvalid | `xsd:boolean` | No | Consente di includere/escludere utenti non validi. |
| companyHandleArray | `types:HandleArray` | No | Filtra i risultati per società. |
| groupHandleArray | `types:HandleArray` | No | Filtra i risultati per gruppo. |
| userRoleArray | `types:StringArray` | No | Filtra i risultati per ruolo utente. |
| charFilterField | `xsd:string` | No | Filtra i risultati in base al prefisso della stringa del campo (vedere [!DNL Trash State).] |
| charFilter | `xsd:string` | No | Filtra i risultati in base a un carattere specifico. |
| sortBy | `xsd:string` | No | Scelta dei campi di ordinamento utente. |
| recordsPerPage | `xsd:int` | No | Restituisce il numero specificato di record per pagina. |
| resultsPage | `xsd:int` | No | Pagina dei risultati. |

**Output (getUsersReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| userArray | `types:UserArray` | Sì | Array di utenti. |

## Esempi {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Questo esempio di codice restituisce l’array di utenti per diversi parametri facoltativi. I ruoli utente, i campi filtro dei caratteri utente e i campi di ordinamento utente sono determinati utilizzando costanti di stringa specifiche.

**Richiesta**

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
