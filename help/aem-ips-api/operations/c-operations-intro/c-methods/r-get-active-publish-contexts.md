---
description: Ottiene un elenco dei contesti di pubblicazione attivi per la società specificata. Un contesto di pubblicazione viene considerato attivo se per il contesto è definito almeno un server attivo.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 9%

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

