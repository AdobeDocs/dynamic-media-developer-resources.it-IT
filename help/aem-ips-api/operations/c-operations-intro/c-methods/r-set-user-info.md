---
description: Imposta gli attributi utente (ad esempio nome, e-mail, ruolo e così via).
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
TQID: 'https://experienceleague.adobe.com/JzJv4nEeWfbY-Wp-qkEq883dlTqaRm9Fc-UvDa70dOg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 10%

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
| defaultRole | `xsd:string` | Sì | Imposta il ruolo di un utente in ogni società a cui appartiene. Si noti, tuttavia, che il ruolo `IpsAdmin` ha la precedenza su altre impostazioni aziendali. |
| passwordExpires | `xsd:dateTime` | No | Imposta la data di scadenza della password. |
| isValid | `xsd:boolean` | Sì | Determina se l&#39;utente è un utente IPS valido. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Sì | Un array di handle aziendali. |

**Output (setUserInfoReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-272c103076fb4de0a53729e2f6bfb895}

**Richiesta**

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
