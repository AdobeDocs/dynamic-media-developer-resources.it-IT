---
description: Associa le impostazioni di configurazione del visualizzatore a una risorsa. Può essere un predefinito per visualizzatori o la risorsa sorgente per il visualizzatore.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic, SDK/API, Predefiniti visualizzatore
role: Developer,Administrator
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 10%

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
