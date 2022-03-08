---
description: Restituisce i gruppi aziendali.
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d98c08a6-4c20-4538-9598-c905078ab7de
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 19%

---

# getGroups{#getgroups}

Restituisce i gruppi aziendali.

Sintassi

## Tipi di utenti autorizzati {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-0e06195f23dd4c69922df210f566dd18}

**Input (getGroupsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Il manico per l&#39;azienda. |

**Output (getGroupsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| groupArray | `types:GroupArray` | Sì | Matrice di gruppi. |

## Esempi {#section-ed0708f611574354bf0c6ea83912b531}

Questo codice restituisce un array contenente tutti i gruppi appartenenti a una società specifica e informazioni specifiche su ciascun gruppo.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getGroupsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupsParam>
```

```java
<getGroupsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle>
         <companyHandle>47</companyHandle>
         <name>MyGroup</name>
         <isSystemDefined>false</isSystemDefined>
      </items>
   </groupArray>
</getGroupsReturn>
```
