---
description: Aggiorna le impostazioni di configurazione del visualizzatore SWF.
seo-description: Aggiorna le impostazioni di configurazione del visualizzatore SWF.
seo-title: updateViewerConfigSettings
solution: Experience Manager
title: updateViewerConfigSettings
topic: Scene7 Image Production System API
uuid: ad4af874-5ca4-4182-868e-afa48b1cd2b6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '65'
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
| ` *`companyHandle`*` | `xsd:string` | Sì | Gestite l&#39;azienda. |
| ` *`assetHandle`*` | `xsd:string` | Sì | Handle risorsa. |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | Sì | Array di impostazioni di configurazione da applicare al visualizzatore. |

**Output (updateViewerConfigSettingsReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.
