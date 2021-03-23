---
description: Solo per uso interno. Gli utenti devono fare riferimento alla sezione Riferimento catalogo immagini di Image Server - Riferimento attributi .
seo-description: Solo per uso interno. Gli utenti devono fare riferimento alla sezione Riferimento catalogo immagini di Image Server - Riferimento attributi .
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 11%

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

Solo per uso interno. Gli utenti devono fare riferimento alla sezione Riferimento catalogo immagini di Image Server - Riferimento attributi .

Sintassi

## Tipi di utenti autorizzati {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-79f0d54acd604ad2a5c96679334f2424}

**Input (getImageServingPublishSettingsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle dell’azienda con le impostazioni di pubblicazione del servizio di immagini. |
| `*`contextHandle`*` | `xsd:string` | Sì | Gestisci il contesto di pubblicazione. |

**Uscita**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | Sì | Array di impostazioni di pubblicazione del server di immagini. |

