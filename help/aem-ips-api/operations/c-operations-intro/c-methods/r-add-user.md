---
description: Crea un account utente e lo aggiunge a una o più società.
seo-description: Crea un account utente e lo aggiunge a una o più società.
seo-title: addUser
solution: Experience Manager
title: addUser
topic: Scene7 Image Production System API
uuid: b8c5ada6-470e-4795-a4f3-20750da709a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addUser{#adduser}

Crea un account utente e lo aggiunge a una o più società.

Quando aggiungete un utente a più società, specificate tali società in base alle relative handle di società in `companyHandleArray`. Questa operazione restituisce l’handle all’utente appena aggiunto.

## Tipi di utenti autorizzati {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-40390a512e314b8d80ecffbb7729f6fb}

**Input (addUserParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`firstName`*` | `xsd:string` | Sì | Nome dell’utente. |
| ` *`lastName`*` | `xsd:string` | Sì | Cognome dell’utente. |
| ` *`e-mail`*` | `xsd:string` | Sì | L&#39;indirizzo e-mail dell&#39;utente. |
| ` *`defaultRole`*` | `xsd:string` | Sì | Imposta il ruolo per un utente in ogni società a cui appartiene. Tuttavia, il `IpsAdmin` ruolo ha la priorità sulle altre impostazioni per società. |
| ` *`password`*` | `xsd:string` | Sì | Imposta la password dell&#39;utente |
| ` *`passwordExpires`*` | `xsd:dateTime` | No | Imposta il periodo di scadenza della password. Specificate il fuso orario al momento del trasferimento della richiesta. I fusi orari sono regolati su Ora centrale. |
| ` *`isInvalid`*` | `xsd:boolean` | Sì | Determina se l&#39;utente è valido. |
| ` *`membershipArray`*` | `xsd:CompanyMembershipUpdateArray` | Sì | Un array di handle della società. |

**Output (addUserParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Sì | L’handle dell’utente. |

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

