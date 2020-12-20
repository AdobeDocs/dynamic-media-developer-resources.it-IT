---
description: Restituisce i gruppi della società.
seo-description: Restituisce i gruppi della società.
seo-title: getGroups
solution: Experience Manager
title: getGroups
topic: Scene7 Image Production System API
uuid: d6e1542d-83a2-4b25-a986-2465e9e5a145
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 18%

---


# getGroups{#getgroups}

Restituisce i gruppi della società.

Sintassi

## Tipi di utenti autorizzati {#section-27c77680a2f34e2f9ecd0af4ebb6847e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-0e06195f23dd4c69922df210f566dd18}

**Input (getGroupsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | L&#39;handle della società. |

**Output (getGroupsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`groupArray`*` | `types:GroupArray` | Sì | Array di gruppi. |

## Esempi {#section-ed0708f611574354bf0c6ea83912b531}

Questo codice restituisce un array che contiene tutti i gruppi appartenenti a una società specifica e informazioni specifiche su ciascun gruppo.

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

