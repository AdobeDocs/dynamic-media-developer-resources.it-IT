---
description: Imposta gli attributi utente (ad esempio nome, e-mail, ruolo, ecc.)
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 14%

---


# setUserInfo{#setuserinfo}

Imposta gli attributi utente (ad esempio nome, e-mail, ruolo, ecc.)

Sintassi

## Tipi di utenti autorizzati {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-71b457921fe74acb862a1e112e550211}

**Input (setUserInfoParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | No | Maniglia utente. |
| `*`firstName`*` | `xsd:string` | Sì | Nome. |
| `*`lastName`*` | `xsd:string` | Sì | Cognome. |
| `*`e-mail`*` | `xsd:string` | Sì | E-mail utente. |
| `*`defaultRole`*` | `xsd:string` | Sì | Imposta il ruolo di un utente in ogni società a cui appartiene. Tuttavia, il ruolo `IpsAdmin` sostituisce altre impostazioni per azienda. |
| `*`passwordExpires`*` | `xsd:dateTime` | No | Data di scadenza della password del set. |
| `*`isValid`*` | `xsd:boolean` | Sì | Determina se l&#39;utente è un utente IPS valido. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sì | Un array di handle aziendali. |

**Output (setUserInfoReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-272c103076fb4de0a53729e2f6bfb895}

**Request Contents (Richiesta contenuto)**

```java
<setUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <firstName>test</firstName>
   <lastName>test</lastName>
   <email>test@test.test</email>
   <defaultRole>IpsAdmin</defaultRole>
   <isValid>true</isValid>
</setUserInfoParam>
```

**Risposta**

Nessuno.
