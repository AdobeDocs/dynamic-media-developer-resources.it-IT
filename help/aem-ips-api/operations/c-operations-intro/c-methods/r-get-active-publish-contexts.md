---
description: Ottiene un elenco di contesti di pubblicazione attivi per la società specificata. Un contesto di pubblicazione viene considerato attivo se è presente almeno un server attivo definito per il contesto.
seo-description: Ottiene un elenco di contesti di pubblicazione attivi per la società specificata. Un contesto di pubblicazione viene considerato attivo se è presente almeno un server attivo definito per il contesto.
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
topic: Scene7 Image Production System API
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# getActivePublishContext{#getactivepublishcontext}

Ottiene un elenco di contesti di pubblicazione attivi per la società specificata. Un contesto di pubblicazione viene considerato attivo se è presente almeno un server attivo definito per il contesto.

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
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società per eseguire query per i contesti di pubblicazione attivi |

**Output (getActivePublishContextsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`contextArray`*` | `types:StringArray` | Sì | Array di contesti di pubblicazione attivi, che possono includere zero o più valori dal contesto di pubblicazione. |

