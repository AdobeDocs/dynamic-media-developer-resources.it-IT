---
description: Ottiene un elenco dei contesti di pubblicazione attivi per la società specificata. Un contesto di pubblicazione viene considerato attivo se per il contesto è definito almeno un server attivo.
seo-description: Ottiene un elenco dei contesti di pubblicazione attivi per la società specificata. Un contesto di pubblicazione viene considerato attivo se per il contesto è definito almeno un server attivo.
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 7%

---


# getActivePublishContext{#getactivepublishcontext}

Ottiene un elenco dei contesti di pubblicazione attivi per la società specificata. Un contesto di pubblicazione viene considerato attivo se per il contesto è definito almeno un server attivo.

Sintassi

## Tipi di utenti autorizzati {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-a4be4024e55c472fa6728faec9c5e048}

**Input (getActivePublishContextsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle dell&#39;azienda per la query dei contesti di pubblicazione attivi |

**Output (getActivePublishContextsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`contextArray`*` | `types:StringArray` | Sì | Array di contesti di pubblicazione attivi, che possono includere zero o più valori dal contesto di pubblicazione. |

