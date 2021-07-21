---
description: Rinomina un progetto.
solution: Experience Manager
title: rinominaProgetto
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 19%

---

# rinominaProgetto{#renameproject}

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

**Input (rinominaProjectParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | Sì | Gestisci l’azienda con il progetto che desideri rinominare. |
| `*`projectHandle`*` | `xsd:string` | Sì | Gestisci il progetto. |
| `*`projectName`*` | `xsd:string` | Sì | Nuovo nome del progetto. |

**Output (ridenominazioneProjectParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | Sì | La gestione del progetto rinominato. |

## Esempi {#section-a0a06d9244774795b695a10b92b2a5e7}

Questo esempio di codice rinomina un progetto e restituisce l&#39;handle di progetto.

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
