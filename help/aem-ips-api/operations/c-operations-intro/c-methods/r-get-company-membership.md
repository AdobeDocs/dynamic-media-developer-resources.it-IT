---
description: Ottiene le appartenenze di un utente in un array aziendale.
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 14%

---

# getCompanyMembership{#getcompanymembership}

Ottiene le appartenenze di un utente in un array aziendale.

Sintassi

## Tipi di utenti autorizzati {#section-f8bba547e1f648648be99dc48fd72b5d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-8745c360c3e1400a88e9bdb26bcb93de}

**Input (getCompanyMembershipParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| userHandle | `xsd:string` | No | Handle per l&#39;utente di cui si desidera ottenere le appartenenze. |

**Output (getCompanyMembershipReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| membershipArray | `types:CompanyMembershipArray` | Sì | Array di appartenenze a società. |

## Esempi {#section-e4958d104ea344a4a79f57d07b46eba7}

Questo esempio di codice prende un handle utente e ottiene tutte le appartenenze dell’utente all’azienda in un array. La risposta è stata troncata per brevità.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
</ns1:getCompanyMembershipParam>
```

**Risposta**

```java
<getCompanyMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <membershipArray>
      <items>
         <companyHandle>48</companyHandle>
         <name>AIR</name>
         <rootPath>AIR/</rootPath>
         <expires>2101-01-31T23:00:00.485-08:00</expires>
      </items>
      ...
    </membershipArray>
</getCompanyMembershipReturn>
```
