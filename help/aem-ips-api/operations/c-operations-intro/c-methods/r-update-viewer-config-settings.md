---
description: Aggiorna le impostazioni di configurazione del visualizzatore SWF.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 11%

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
| companyHandle | `xsd:string` | Sì | Gestire l&#39;azienda. |
| assetHandle | `xsd:string` | Sì | Handle risorsa. |
| configSettingArray | `types:ConfigSettingArray` | Sì | Matrice di impostazioni di configurazione da applicare al visualizzatore. |

**Output (updateViewerConfigSettingsReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.
