---
description: Rinomina un progetto.
seo-description: Rinomina un progetto.
seo-title: renameProject
solution: Experience Manager
title: renameProject
topic: Scene7 Image Production System API
uuid: 6303c493-a6fe-4b32-80c3-947aba4190f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

---


# renameProject{#renameproject}

Rinomina un progetto.

Sintassi

## Tipi di utenti autorizzati {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-43ccd77648784be4a259a723c3e1db40}

**Input (renameProjectParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | Sì | Gestite la società con il progetto da rinominare. |
| ` *`projectHandle`*` | `xsd:string` | Sì | Gestite il progetto. |
| ` *`projectName`*` | `xsd:string` | Sì | Nuovo nome progetto. |

**Output (renameProjectParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`projectHandle`*` | `xsd:string` | Sì | L&#39;handle del progetto rinominato. |

## Esempi {#section-a0a06d9244774795b695a10b92b2a5e7}

Questo esempio di codice rinomina un progetto e restituisce l’handle del progetto.

**Request Contents (Richiesta contenuto)**

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**Risposta**

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```

