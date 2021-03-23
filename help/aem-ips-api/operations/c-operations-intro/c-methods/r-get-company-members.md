---
description: Restituisce gli utenti di una società specificata da un handle aziendale.
seo-description: Restituisce gli utenti di una società specificata da un handle aziendale.
seo-title: getCompanyMembers
solution: Experience Manager
title: getCompanyMembers
uuid: 45e2d040-a70a-46f4-863a-633ddabcbcf6
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 12%

---


# getCompanyMembers{#getcompanymembers}

Restituisce gli utenti di una società specificata da un handle aziendale.

Sintassi

## Tipi di utenti autorizzati {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-5602e4d6f2214e398e6a804e61f1a088}

**Input (getCompanyMembersParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle dell&#39;azienda di cui si desidera ottenere i membri. |
| `*`includeInvalid`*` | `xsd:boolean` | Sì | Includi società non valide. |

**Output (getCompanyMembersReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`MemberArray`*` | `types:CompanyMemberArray` | Sì | Array di appartenenze utente. |

## Esempi {#section-39d8cf3653fd4fe8b842caabac9dedfc}

Questo esempio di codice restituisce tutti i membri di una società in un array di utenti. La risposta è stata troncata per brevità.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getCompanyMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getCompanyMembersParam>
```

**Risposta**

```java
<getCompanyMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray>
      <items>
         <userHandle>66|pbayol@adobe.com</userHandle>
         <firstName>Peter</firstName>
         <lastName>Bayol</lastName>
         <email>pbayol@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-25T23:12:49.472-07:00</passwordExpires>
      </items>
      ...
   </memberArray>
</getCompanyMembersReturn>
```

