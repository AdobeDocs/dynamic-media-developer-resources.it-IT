---
description: Solo per uso interno. Consulta la sezione Attributi del catalogo di riferimento del materiale di rendering delle immagini .
seo-description: Solo per uso interno. Consulta la sezione Attributi del catalogo di riferimento del materiale di rendering delle immagini .
seo-title: getImageRenderingPublishSettings
solution: Experience Manager
title: getImageRenderingPublishSettings
uuid: b1c253b5-febe-4dc7-95a1-a5f4789030e7
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 12%

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

