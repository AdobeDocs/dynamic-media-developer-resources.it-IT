---
description: Solo per uso interno. Consulta la sezione Attributi del catalogo di riferimento del materiale di rendering delle immagini .
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 15%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Solo per uso interno. Consulta la sezione Attributi del catalogo di riferimento del materiale di rendering delle immagini .

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
| `*`companyHandle`*` | `xsd:string` | Sì | L’handle dell’azienda di cui desideri ottenere le impostazioni di pubblicazione del rendering delle immagini. |
| `*`contextHandle`*` | `xsd:string` | Sì | Gestisci il contesto di pubblicazione. |

**Output (getImageRenderingPublishSettingsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | Sì | Impostazioni di pubblicazione del rendering delle immagini. |
