---
description: Aggiorna le impostazioni di configurazione del visualizzatore SWF.
seo-description: Aggiorna le impostazioni di configurazione del visualizzatore SWF.
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
feature: Dynamic Media Classic, SDK/API, Predefiniti visualizzatore
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 10%

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
