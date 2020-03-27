---
description: Ottiene un array di utenti secondo quanto specificato dalle handle di società, gruppo e ruolo utente. Questa operazione consente di ordinare gli utenti restituiti e filtrare per carattere.
seo-description: Ottiene un array di utenti secondo quanto specificato dalle handle di società, gruppo e ruolo utente. Questa operazione consente di ordinare gli utenti restituiti e filtrare per carattere.
seo-title: getUsers
solution: Experience Manager
title: getUsers
topic: Scene7 Image Production System API
uuid: f16ccd1b-0f00-4d9a-b6e1-6abc3bde1af9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getUsers{#getusers}

Ottiene un array di utenti secondo quanto specificato dalle handle di società, gruppo e ruolo utente. Questa operazione consente di ordinare gli utenti restituiti e filtrare per carattere.

## Tipi di utenti autorizzati {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`includeInactive`*` | `xsd:boolean` | No | Includere o escludere utenti inattivi. Gli utenti amministratore non IPS devono essere membri attivi di almeno una società per essere autorizzati a effettuare chiamate API. Se l&#39;utente non dispone di appartenenze attive alla società, verrà restituito un errore di autorizzazione. |
| ` *`includeInvalid`*` | `xsd:boolean` | No | Consente di includere/escludere utenti non validi. |
| ` *`companyHandleArray`*` | `types:HandleArray` | No | Filtrare i risultati per società. |
| ` *`groupHandleArray`*` | `types:HandleArray` | No | Filtrare i risultati per gruppo. |
| ` *`userRoleArray`*` | `types:StringArray` | No | Filtrare i risultati per ruolo utente. |
| ` *`charFilterField`*` | `xsd:string` | No | Filtra i risultati in base al prefisso della stringa del campo (vedere [!DNL Trash State).] |
| ` *`charFilter`*` | `xsd:string` | No | Filtrare i risultati in base a un carattere specifico. |
| ` *`sortBy`*` | `xsd:string` | No | Scelta dei campi di ordinamento utente. |
| ` *`recordsPerPage`*` | `xsd:int` | No | Restituisce il numero specificato di record per pagina. |
| ` *`resultPage`*` | `xsd:int` | No | Pagina dei risultati. |

**Output (getUsersReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`userArray`*` | `types:UserArray` | Sì | Un array di utenti. |

## Esempi {#section-bc43a5dd7b4c4f048d25fc881554dab2}

Questo esempio di codice restituisce l&#39;array di utenti per diversi parametri facoltativi. I ruoli utente, i campi del filtro dei caratteri utente e i campi di ordinamento utente sono determinati utilizzando costanti stringa specifiche.

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

