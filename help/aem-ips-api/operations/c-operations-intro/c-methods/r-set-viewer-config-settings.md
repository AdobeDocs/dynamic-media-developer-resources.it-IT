---
description: Allega le impostazioni di configurazione del visualizzatore a una risorsa. Possono essere un predefinito visualizzatore o la risorsa sorgente del visualizzatore.
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
TQID: 'https://experienceleague.adobe.com/MX6dj-7j6HfNSISaWFheorOZYVnszSY24OuuUGdKvPA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
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
| configSettingArray | `types:ConfigSettingArray` | Sì | Matrice di `ConfigSettings` applicata alla risorsa. |

**Output (setViewerConfigSettingsParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.
