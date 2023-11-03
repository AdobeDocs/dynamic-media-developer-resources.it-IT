---
description: Imposta gli attributi utente (ad esempio nome, e-mail, ruolo e così via).
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 13%

---

# setUserInfo{#setuserinfo}

Imposta gli attributi utente (ad esempio nome, e-mail, ruolo e così via).

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
| userHandle | `xsd:string` | No | Handle utente. |
| firstName | `xsd:string` | Sì | Nome. |
| lastName | `xsd:string` | Sì | Cognome. |
| email | `xsd:string` | Sì | E-mail utente. |
| defaultRole | `xsd:string` | Sì | Imposta il ruolo di un utente in ogni società a cui appartiene. Si noti tuttavia che `IpsAdmin` il ruolo sostituisce altre impostazioni per società. |
| passwordExpires | `xsd:dateTime` | No | Imposta la data di scadenza della password. |
| isValid | `xsd:boolean` | Sì | Determina se l&#39;utente è un utente IPS valido. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Sì | Un array di handle aziendali. |

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
