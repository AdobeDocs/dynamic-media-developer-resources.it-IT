---
description: Imposta gli attributi utente (ad esempio nome, e-mail, ruolo, ecc.)
seo-description: Imposta gli attributi utente (ad esempio nome, e-mail, ruolo, ecc.)
seo-title: setUserInfo
solution: Experience Manager
title: setUserInfo
topic: Scene7 Image Production System API
uuid: 52e3a21e-1dd5-4f9d-b460-506d280fff47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`userHandle`*` | `xsd:string` | No | handle utente. |
| ` *`firstName`*` | `xsd:string` | Sì | Nome. |
| ` *`lastName`*` | `xsd:string` | Sì | Cognome. |
| ` *`e-mail`*` | `xsd:string` | Sì | E-mail utente. |
| ` *`defaultRole`*` | `xsd:string` | Sì | Imposta il ruolo per un utente in ogni società a cui appartiene. Tuttavia, il `IpsAdmin` ruolo ha la priorità sulle altre impostazioni per società. |
| ` *`passwordExpires`*` | `xsd:dateTime` | No | Data di scadenza della password del set. |
| ` *`isInvalid`*` | `xsd:boolean` | Sì | Determina se l&#39;utente è un utente IPS valido. |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sì | Un array di handle della società. |

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
