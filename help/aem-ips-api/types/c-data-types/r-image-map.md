---
description: Esegui il targeting per un’azione di clic nel browser.
solution: Experience Manager
title: Mappa immagine
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 5%

---

# [!DNL ImageMap]{#imagemap}

Esegui il targeting per un’azione di clic nel browser.

Sempre associato a un&#39;immagine. Puoi ottenere un `ImageMap` target da `ImageInfo`.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| imageMapHandle | `xsd:string` | Handle mappa immagine. |
| [!DNL name] | `xsd:string` | Nome mappa immagine. |
| [!DNL region] | `xsd:string` | Coordinate mappa immagine. Il formato è basato sul HTML `<area>` attributo tag. |
| [!DNL action] | `xsd:string` | Altri attributi da includere nel HTML `<area>` , incluso `href` URL. |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] valore. |
| [!DNL position] | `xsd:string` | Posizione nel formato del HTML `<area>` dell&#39;elemento [!DNL coords] attributo. Ad esempio: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | True se la mappa immagine è abilitata. |
| lastModified | `xsd:dateTime` | Data e ora dell&#39;ultima modifica apportata alla mappa immagine. |
