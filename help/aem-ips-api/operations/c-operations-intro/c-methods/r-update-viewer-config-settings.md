---
description: Aggiorna le impostazioni di configurazione del visualizzatore SWF.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic, SDK/API, Predefiniti visualizzatore
role: Developer,Administrator
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 12%

---

# updateViewerConfigSettings{#updateviewerconfigsettings}

Aggiorna le impostazioni di configurazione del visualizzatore SWF.

Sintassi

## Tipi di utenti autorizzati {#section-0dd001da1b784aefa5eb5b50c7a2c045}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-29790d933fb24aa392d0cb2d52d1310f}

**Input (updateViewerConfigSettingsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Manda all&#39;azienda. |
| `*`assetHandle`*` | `xsd:string` | Sì | Gestione risorse. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Sì | Array di impostazioni di configurazione da applicare al visualizzatore. |

**Output (updateViewerConfigSettingsReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.
