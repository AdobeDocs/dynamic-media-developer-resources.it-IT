---
description: Solo per uso interno. Consultate la sezione Attributi del catalogo di riferimento del materiale di rendering delle immagini.
seo-description: Solo per uso interno. Consultate la sezione Attributi del catalogo di riferimento del materiale di rendering delle immagini.
seo-title: getImageRenderingPublishSettings
solution: Experience Manager
title: getImageRenderingPublishSettings
topic: Scene7 Image Production System API
uuid: b1c253b5-febe-4dc7-95a1-a5f4789030e7
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

Solo per uso interno. Consultate la sezione Attributi del catalogo di riferimento del materiale di rendering delle immagini.

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
| ` *`companyHandle`*` | `xsd:string` | Sì | L’handle della società di cui desiderate ottenere le impostazioni di pubblicazione del rendering delle immagini. |
| ` *`contextHandle`*` | `xsd:string` | Sì | Consente di passare al contesto di pubblicazione. |

**Output (getImageRenderingPublishSettingsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`publishSettingsArray`*` | `type:ConfigSettingArray` | Sì | Impostazioni di pubblicazione del rendering delle immagini. |

