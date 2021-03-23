---
description: Associa le impostazioni di configurazione del visualizzatore a una risorsa. Può essere un predefinito per visualizzatori o la risorsa sorgente per il visualizzatore.
seo-description: Associa le impostazioni di configurazione del visualizzatore a una risorsa. Può essere un predefinito per visualizzatori o la risorsa sorgente per il visualizzatore.
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
uuid: d83d866e-9243-479f-9b33-727aad8158e5
feature: Dynamic Media Classic, SDK/API, Predefiniti visualizzatore
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 8%

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
