---
description: Ottiene tutte le impostazioni di configurazione del visualizzatore associate alla risorsa specificata.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
TQID: 'https://experienceleague.adobe.com/GeSAS1EP7Q6EgsQltyC-TVnxS0zusuKxKs6QL8wfLWw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 17%

---

# getViewerConfigSettings{#getviewerconfigsettings}

Ottiene tutte le impostazioni di configurazione del visualizzatore associate alla risorsa specificata.

Sintassi

## Tipi di utenti autorizzati {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-7d06abf3d707494c8a1270c7fa1477f1}

**Input (getViewerConfigSettingsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Gestire l&#39;azienda. |
| assetHandle | `xsd:string` | Sì | Gestisci la risorsa. |

**Output (getViewerCoinfigSettingsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| tipo | `xsd:string` | Sì | Tipo di visualizzatore a cui si applicano le impostazioni di configurazione. |
| configSettingsArray | `types:ConfigSettingsArray` | Sì | Array delle impostazioni di configurazione del visualizzatore. |
