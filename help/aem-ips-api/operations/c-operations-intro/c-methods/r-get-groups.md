---
description: Restituisce i gruppi di società.
solution: Experience Manager
title: getGroups
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d98c08a6-4c20-4538-9598-c905078ab7de
TQID: 'https://experienceleague.adobe.com/QyPdrXDIqo4P081BxGGFD-a53PcviQlNumVqwvEsNc8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 61
ht-degree: 16%

---

# getGroups{#getgroups}

Restituisce i gruppi di società.

Sintassi

## Tipi di utenti autorizzati {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-0e06195f23dd4c69922df210f566dd18}

**Input (getGroupsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | La maniglia per l&#39;azienda. |

**Output (getGroupsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| groupArray | `types:GroupArray` | Sì | Array di gruppi. |

## Esempi {#section-ed0708f611574354bf0c6ea83912b531}

Questo codice restituisce un array che contiene tutti i gruppi che appartengono a una società specifica e informazioni specifiche su ciascun gruppo.

**Richiesta**

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
