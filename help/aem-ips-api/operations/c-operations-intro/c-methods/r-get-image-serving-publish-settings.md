---
description: Solo per uso interno. Gli utenti devono fare riferimento alla sezione Riferimento catalogo immagini di Image Server - Riferimento attributi .
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 14%

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
