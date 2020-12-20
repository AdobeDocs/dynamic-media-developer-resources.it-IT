---
description: Restituisce i membri di un gruppo.
seo-description: Restituisce i membri di un gruppo.
seo-title: getGroupMembership
solution: Experience Manager
title: getGroupMembership
topic: Scene7 Image Production System API
uuid: 5ec48e8c-378b-43a3-b3dc-aa21dbf339b5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 16%

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
| ` *`userHandle`*` | `xsd:string` | No | L’handle dell’utente. |
| ` *`companyHandle`*` | `xsd:string` | No | L&#39;handle della società. |

**Output (getGroupMembershipReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`groupArray`*` | `types:GroupArray` | Sì | Array di gruppi. |

## Esempi {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Questo esempio di codice restituisce tutti i membri di un gruppo. Poiché le maniglie della società e dell’utente sono facoltative, l’operazione può restituire tutti i membri di tutti i gruppi.

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

