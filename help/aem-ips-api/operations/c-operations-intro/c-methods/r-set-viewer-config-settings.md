---
description: Associa le impostazioni di configurazione del visualizzatore a una risorsa. Può essere un predefinito per visualizzatori o la risorsa sorgente per il visualizzatore.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 9%

---


# setViewerConfigSettings{#setviewerconfigsettings}

Associa le impostazioni di configurazione del visualizzatore a una risorsa. Può essere un predefinito per visualizzatori o la risorsa sorgente per il visualizzatore.

Sintassi

## Tipi di utenti autorizzati {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-bcc8c83cc84141e8b1341be9133e8511}

**Input (setViewerConfigSettingsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Manda all&#39;azienda. |
| `*`assetHandle`*` | `xsd:string` | Sì | Gestione risorse. |
| `*`name`*` | `xsd:string` | Sì | Nome risorsa. |
| `*`type`*` | `xsd:string` | Sì | Il tipo di risorsa a cui applicare la configurazione del visualizzatore. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Sì | Matrice di `ConfigSettings` applicata alla risorsa. |

**Output (setViewerConfigSettingsParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.
