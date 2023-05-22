---
description: Solo per uso interno. Consultate la sezione Image Rendering Material Catalog Reference-Catalog Attributes.
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 14%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Solo per uso interno. Consultate la sezione Image Rendering Material Catalog Reference-Catalog Attributes.

Sintassi

## Tipi di utenti autorizzati {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-4f2cb8c589384816bb2525654ec49963}

**Input (getImageRenderingPublishSettingsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle per l’azienda di cui desideri ottenere le impostazioni di pubblicazione per il rendering immagini. |
| contextHandle | `xsd:string` | Sì | Gestisci per il contesto di pubblicazione. |

**Output (getImageRenderingPublishSettingsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| publishSettingsArray | `type:ConfigSettingArray` | Sì | Impostazioni di pubblicazione del rendering immagini. |
