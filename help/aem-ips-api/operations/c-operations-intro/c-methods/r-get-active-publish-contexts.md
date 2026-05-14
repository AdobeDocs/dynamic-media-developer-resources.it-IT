---
description: Ottiene un elenco di contesti di pubblicazione attivi per la società specificata. Un contesto di pubblicazione viene considerato attivo se per il contesto è definito almeno un server attivo.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
TQID: 'https://experienceleague.adobe.com/g337PVX5asvB-o-VQL0XA5XSrgQ0c2vx0xC4-93Dm8E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 9%

---

# getActivePublishContext{#getactivepublishcontext}

Ottiene un elenco di contesti di pubblicazione attivi per la società specificata. Un contesto di pubblicazione viene considerato attivo se per il contesto è definito almeno un server attivo.

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
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda per la query dei contesti di pubblicazione attivi |

**Output (getActivePublishContextsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| contextArray | `types:StringArray` | Sì | Matrice di contesti di pubblicazione attivi, che possono includere zero o più valori da Contesto di pubblicazione. |
