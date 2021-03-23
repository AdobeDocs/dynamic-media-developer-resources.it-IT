---
description: Restituisce i membri di un gruppo.
seo-description: Restituisce i membri di un gruppo.
seo-title: getGroupMembership
solution: Experience Manager
title: getGroupMembership
uuid: 5ec48e8c-378b-43a3-b3dc-aa21dbf339b5
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 14%

---


# getGroupMembership{#getgroupmembership}

Restituisce i membri di un gruppo.

Sintassi

## Tipi di utenti autorizzati {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-2e92f850254e46e48403acaa215341a5}

**Input (getGroupMembershipParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | No | L&#39;handle dell&#39;utente. |
| `*`companyHandle`*` | `xsd:string` | No | Il manico per l&#39;azienda. |

**Output (getGroupMembershipReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | Sì | Matrice di gruppi. |

## Esempi {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Questo esempio di codice restituisce tutti i membri di un gruppo. Poiché gli handle dell&#39;azienda e dell&#39;utente sono facoltativi, l&#39;operazione può restituire tutti i membri di tutti i gruppi.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**Risposta**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```

