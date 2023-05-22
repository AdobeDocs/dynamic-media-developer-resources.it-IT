---
description: Allega le impostazioni di configurazione del visualizzatore a una risorsa. Possono essere un predefinito visualizzatore o la risorsa sorgente del visualizzatore.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 8%

---

# setViewerConfigSettings{#setviewerconfigsettings}

Allega le impostazioni di configurazione del visualizzatore a una risorsa. Possono essere un predefinito visualizzatore o la risorsa sorgente del visualizzatore.

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
| companyHandle | `xsd:string` | Sì | Gestire l&#39;azienda. |
| assetHandle | `xsd:string` | Sì | Handle risorsa. |
| nome | `xsd:string` | Sì | Nome risorsa. |
| tipo | `xsd:string` | Sì | Tipo di risorsa a cui applicare la configurazione del visualizzatore. |
| configSettingArray | `types:ConfigSettingArray` | Sì | L’array di `ConfigSettings` applicato alla risorsa. |

**Output (setViewerConfigSettingsParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.
