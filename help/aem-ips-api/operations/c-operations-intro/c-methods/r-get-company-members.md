---
description: Restituisce gli utenti di una società specificata da un handle aziendale.
solution: Experience Manager
title: getCompanyMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da5e5a48-2e0b-4ccc-a71e-b5b746484d4a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '89'
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
| CompanyHandle | `xsd:string` | Sì | L&#39;handle per la società di cui si desidera ottenere membri. |
| includeInvalid | `xsd:boolean` | Sì | Includi non valido società. |

**Output (getCompanyMembersReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| memberArray | `types:CompanyMemberArray` | Sì | Matrice di utente appartenenze. |

## Esempi {#section-39d8cf3653fd4fe8b842caabac9dedfc}

In questo esempio di codice vengono restituiti tutti i membri di una società in una matrice utente. La risposta è stata troncata per brevità.

**Richiesta**

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
