---
description: Ottiene un elenco dei caratteri utilizzati in un campo specifico.
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 10%

---


# getUserChars{#getuserchars}

Ottiene un elenco dei caratteri utilizzati in un campo specifico.

Sintassi

## Tipi di utenti autorizzati {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-93107d87f1b24fc8ad276dfee5e30b63}

**Input (getUserCharsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`charField`*` | `xsd:string` | Sì | Determina lo stato del cestino da cercare. |
| `*`includeInactive`*` | `xsd:boolean` | Sì | Includi o escludi gli utenti inattivi. Gli utenti amministratori non IPS devono essere membri attivi di almeno una società per essere autorizzati a effettuare chiamate API. Se l&#39;utente non dispone di appartenenze attive alla società, verrà restituito un errore di autorizzazione. |
| `*`includInvalid`*` | `xsd:boolean` | No | Includere o escludere utenti non validi. |
| `*`companyHandleArray`*` | `types:HandleArray` | No | Filtrare i risultati in base all’azienda. |
| `*`groupHandleArray`*` | `types:HandleArray` | No | Filtra i risultati in base ai gruppi. |
| `*`userRoleArray`*` | `types:StringArray` | No | Filtra i risultati in base al ruolo dell’utente. |
| `*`numChars`*` | `xsd:int` | No | Abilita >1 carattere. |

**Output (getUserCharsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`userCharsArray`*` | `types:StringArray` | Sì | Matrice di prefissi di caratteri. |

## Esempi {#section-3702f165e8b041139a6144f4a76ca25f}

Questo esempio di codice restituisce:

* Primi caratteri dei cognomi degli utenti di una specifica azienda.
* Un insieme di gruppi.
* Un insieme di ruoli utente.

La costante della stringa Campi filtro caratteri utente determina il tipo di caratteri utente restituiti.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**Risposta**

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```

