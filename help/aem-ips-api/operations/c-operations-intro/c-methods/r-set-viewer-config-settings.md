---
description: Associa le impostazioni di configurazione del visualizzatore a una risorsa. Possono essere un predefinito per visualizzatori o la risorsa sorgente per il visualizzatore.
seo-description: Associa le impostazioni di configurazione del visualizzatore a una risorsa. Possono essere un predefinito per visualizzatori o la risorsa sorgente per il visualizzatore.
seo-title: setViewerConfigSettings
solution: Experience Manager
title: setViewerConfigSettings
topic: Scene7 Image Production System API
uuid: d83d866e-9243-479f-9b33-727aad8158e5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setViewerConfigSettings{#setviewerconfigsettings}

Associa le impostazioni di configurazione del visualizzatore a una risorsa. Possono essere un predefinito per visualizzatori o la risorsa sorgente per il visualizzatore.

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
| ` *`companyHandle`*` | `xsd:string` | Sì | Gestite l&#39;azienda. |
| ` *`assetHandle`*` | `xsd:string` | Sì | Handle risorsa. |
| ` *`name`*` | `xsd:string` | Sì | Nome risorsa. |
| ` *`type`*` | `xsd:string` | Sì | Il tipo di risorsa a cui applicare la configurazione del visualizzatore. |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | Sì | L’array di risorse `ConfigSettings` applicate alla risorsa. |

**Output (setViewerConfigSettingsParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.
