---
description: Ottiene un elenco dei caratteri utilizzati in un particolare campo.
seo-description: Ottiene un elenco dei caratteri utilizzati in un particolare campo.
seo-title: getUserChars
solution: Experience Manager
title: getUserChars
topic: Scene7 Image Production System API
uuid: c9fa7826-5174-4298-99e6-a0627e432567
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 10%

---


# getUserChars{#getuserchars}

Ottiene un elenco dei caratteri utilizzati in un particolare campo.

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
| ` *`charField`*` | `xsd:string` | Sì | Determina lo stato del cestino da cercare. |
| ` *`includeInactive`*` | `xsd:boolean` | Sì | Includere o escludere utenti inattivi. Gli utenti amministratore non IPS devono essere membri attivi di almeno una società per essere autorizzati a effettuare chiamate API. Se l&#39;utente non dispone di appartenenze attive alla società, verrà restituito un errore di autorizzazione. |
| ` *`includInvalid`*` | `xsd:boolean` | No | Includere o escludere utenti non validi. |
| ` *`companyHandleArray`*` | `types:HandleArray` | No | Filtrare i risultati in base alla società. |
| ` *`groupHandleArray`*` | `types:HandleArray` | No | Filtra i risultati in base ai gruppi. |
| ` *`userRoleArray`*` | `types:StringArray` | No | Filtra i risultati in base al ruolo utente. |
| ` *`numChars`*` | `xsd:int` | No | Abilitare >1 carattere. |

**Output (getUserCharsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`userCharsArray`*` | `types:StringArray` | Sì | Un array di prefissi di caratteri. |

## Esempi {#section-3702f165e8b041139a6144f4a76ca25f}

Questo esempio di codice restituisce:

* Primi caratteri dei cognomi degli utenti di una specifica società.
* Un insieme di gruppi.
* Un set di ruoli utente.

La costante stringa Campi filtro carattere utente determina il tipo di caratteri utente restituiti.

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

