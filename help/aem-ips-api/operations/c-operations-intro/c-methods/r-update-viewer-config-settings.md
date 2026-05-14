---
description: Aggiorna le impostazioni di configurazione del visualizzatore SWF.
solution: Experience Manager
title: updateViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 04565e2b-bda3-4ad0-afc1-2df01e455490
TQID: 'https://experienceleague.adobe.com/YcfK5U6MKvmV2ulOQ3s2sOOBsgASSeslCIrk87xLAv8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 59
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
