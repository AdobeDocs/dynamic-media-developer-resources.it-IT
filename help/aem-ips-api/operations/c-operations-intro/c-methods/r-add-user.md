---
description: Crea un account utente e lo aggiunge a una o più società.
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: aed39e73-f528-4c26-8f62-c3d796e9101a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 12%

---

# addUser{#adduser}

Crea un account utente e lo aggiunge a una o più società.

Quando aggiungi un utente a più società, specifica tali società in base ai relativi handle aziendali in `companyHandleArray`. Questa operazione restituisce l&#39;handle all&#39;utente appena aggiunto.

## Tipi di utenti autorizzati {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-40390a512e314b8d80ecffbb7729f6fb}

**Input (addUserParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`firstName`*` | `xsd:string` | Sì | Nome dell&#39;utente. |
| `*`lastName`*` | `xsd:string` | Sì | Cognome dell&#39;utente. |
| `*`e-mail`*` | `xsd:string` | Sì | L’indirizzo e-mail dell’utente. |
| `*`defaultRole`*` | `xsd:string` | Sì | Imposta il ruolo di un utente in ogni società a cui appartiene. Tuttavia, il ruolo `IpsAdmin` sostituisce altre impostazioni per azienda. |
| `*`password`*` | `xsd:string` | Sì | Imposta la password dell&#39;utente |
| `*`passwordExpires`*` | `xsd:dateTime` | No | Imposta il periodo di scadenza della password. Specifica il fuso orario quando viene trasmessa la richiesta. I fusi orari sono regolati su Ora centrale. |
| `*`isValid`*` | `xsd:boolean` | Sì | Determina se l&#39;utente è valido. |
| `*`membershipArray`*` | `xsd:CompanyMembershipUpdateArray` | Sì | Un array di handle aziendali. |

**Output (addUserParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Sì | L&#39;handle dell&#39;utente. |

## Esempi {#section-2547cef622734b71919eef849960b5cb}

L&#39;API IPS restituisce un elemento handle utente che specifica il nuovo utente.

**Request Contents (Richiesta contenuto)**

```java
<ns1:addUserParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:firstName>Joe</ns1:firstName>
   <ns1:lastName>User</ns1:lastName>
   <ns1:email>juser@adobe.com</ns1:email>
   <ns1:defaultRole>TrialSiteUser</ns1:role>
   <ns1:password>passw0rd</ns1:password>
   <ns1:isValid>true</ns1:isValid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addUserParam>
```

**Risposta**

```java
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```
