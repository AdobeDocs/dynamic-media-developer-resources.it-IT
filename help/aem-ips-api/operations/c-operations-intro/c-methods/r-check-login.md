---
description: Controlla se un utente con una società specifica (identificata da un handle), un indirizzo e-mail e una password può effettuare l’accesso.
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f96f376-574c-464b-9c89-c215f6454b81
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 8%

---

# checkLogin{#checklogin}

Controlla se un utente con una società specifica (identificata da un handle), un indirizzo e-mail e una password può effettuare l’accesso.

>[!NOTE]
>
>Se l&#39;handle della società viene omesso, questo metodo controlla l&#39;accesso dell&#39;utente predefinito.

## Tipi di utenti autorizzati {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-1ad4c0b4803b4388aedd655030676cb3}

**Input (checkLoginParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | No | Handle per l&#39;azienda che contiene l&#39;utente. |
| email | `xsd:string` | Sì | Indirizzo e-mail dell’utente. |
| password | `xsd:string` | Sì | La password dell&#39;utente. |

**Output (checkLoginParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| stato | `xsd:string` | Sì | Stato di accesso dell&#39;utente. |

## Esempi {#section-23f90100a9d94bc7b4045634cccd1b98}

Questo codice di esempio utilizza un parametro dell&#39;handle aziendale, un indirizzo e-mail e una password per determinare se un utente può accedere a IPS. Se l&#39;utente *può* accedere, questo metodo restituisce la stringa `ValidLogin`. Se l&#39;utente *non può* accedere, questo metodo restituisce la stringa `InvalidLogin`.

**Richiesta**

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**Risposta**

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```
