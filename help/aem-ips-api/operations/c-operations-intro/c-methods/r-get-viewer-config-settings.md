---
description: Ottiene tutte le impostazioni di configurazione del visualizzatore associate alla risorsa specificata.
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic, SDK/API, Predefiniti visualizzatore
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 16%

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
| `*`companyHandle`*` | `xsd:string` | Sì | Manda all&#39;azienda. |
| `*`assetHandle`*` | `xsd:string` | Sì | Gestisci la risorsa. |

**Output (getViewerConfigSettingsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`type`*` | `xsd:string` | Sì | Tipo di visualizzatore a cui si applicano le impostazioni di configurazione. |
| `*`configSettingsArray`*` | `types:ConfigSettingsArray` | Sì | Array di impostazioni di configurazione del visualizzatore. |

