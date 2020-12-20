---
description: Solo per uso interno. Gli utenti devono fare riferimento alla sezione Riferimento per il catalogo immagini di Image Server - Riferimento attributo.
seo-description: Solo per uso interno. Gli utenti devono fare riferimento alla sezione Riferimento per il catalogo immagini di Image Server - Riferimento attributo.
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
topic: Scene7 Image Production System API
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 12%

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

Solo per uso interno. Gli utenti devono fare riferimento alla sezione Riferimento per il catalogo immagini di Image Server - Riferimento attributo.

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
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società con le impostazioni di pubblicazione di gestione delle immagini. |
| ` *`contextHandle`*` | `xsd:string` | Sì | Consente di passare al contesto di pubblicazione. |

**Uscita**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`publishSettingArray`*` | `xsd:string` | Sì | Array di impostazioni di pubblicazione del server immagini. |

