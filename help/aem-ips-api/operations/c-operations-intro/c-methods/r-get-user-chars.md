---
description: Ottiene un elenco dei caratteri utilizzati in un campo specifico.
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '174'
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
| charField | `xsd:string` | Sì | Determina lo stato del cestino da cercare. |
| includeInactive | `xsd:boolean` | Sì | Includere o escludere gli utenti inattivi. Per poter essere autorizzati a effettuare chiamate API, gli utenti non amministratori IPS devono essere membri attivi di almeno una società. Se l&#39;utente non dispone di appartenenze aziendali attive, viene restituito un errore di autorizzazione. |
| includeInvalid | `xsd:boolean` | No | Includere o escludere utenti non validi. |
| companyHandleArray | `types:HandleArray` | No | Filtra i risultati in base alla società. |
| groupHandleArray | `types:HandleArray` | No | Filtra i risultati in base ai gruppi. |
| userRoleArray | `types:StringArray` | No | Filtra i risultati in base al ruolo utente. |
| numChars | `xsd:int` | No | Attiva >1 carattere. |

**Output (getUserCharsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| userCharsArray | `types:StringArray` | Sì | Matrice di prefissi di caratteri. |

## Esempi {#section-3702f165e8b041139a6144f4a76ca25f}

Questo esempio di codice restituisce:

* Primi caratteri dei cognomi degli utenti di una specifica azienda.
* Un insieme di gruppi.
* Un set di ruoli utente.

La costante stringa Campi filtro caratteri utente determina il tipo di caratteri utente restituiti.

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
