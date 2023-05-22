---
description: Solo per uso interno. Gli utenti devono fare riferimento alla sezione Riferimento catalogo immagini Image Server - Riferimento attributo.
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 13%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

Solo per uso interno. Gli utenti devono fare riferimento alla sezione Riferimento catalogo immagini Image Server - Riferimento attributo.

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
| companyHandle | `xsd:string` | Sì | Handle per l’azienda con le impostazioni di pubblicazione di server immagini. |
| contextHandle | `xsd:string` | Sì | Gestisci per il contesto di pubblicazione. |

**Output**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| publishSettingArray | `xsd:string` | Sì | Array delle impostazioni di pubblicazione del server immagini. |
