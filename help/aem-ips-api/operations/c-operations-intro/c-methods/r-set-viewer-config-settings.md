---
description: Associa le impostazioni di configurazione del visualizzatore a una risorsa. Può essere un predefinito per visualizzatori o la risorsa sorgente per il visualizzatore.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 11%

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
| companyHandle | `xsd:string` | Sì | Manda all&#39;azienda. |
| assetHandle | `xsd:string` | Sì | Gestione risorse. |
| name | `xsd:string` | Sì | Nome risorsa. |
| Testo | `xsd:string` | Sì | Il tipo di risorsa a cui applicare la configurazione del visualizzatore. |
| configSettingArray | `types:ConfigSettingArray` | Sì | L&#39;array di `ConfigSettings` applicato alla risorsa. |

**Output (setViewerConfigSettingsParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.
