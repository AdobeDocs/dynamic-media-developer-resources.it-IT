---
description: Individua un’azione di clic nel browser.
solution: Experience Manager
title: Mappa immagine
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 11%

---

# Mappa immagine{#imagemap}

Individua un’azione di clic nel browser.

Sempre associata a un&#39;immagine. Puoi ottenere un `ImageMap` target da `ImageInfo`.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| imageMapHandle | `xsd:string` | Maniglia mappa immagine. |
| name | `xsd:string` | Nome mappa immagine. |
| regione | `xsd:string` | Coordinate mappa immagine. Il formato è basato su HTML `<area>` attributo tag. |
| action | `xsd:string` | Altri attributi da includere in HTML `<area>` , compreso il `href` URL. |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] valore. |
| position | `xsd:string` | Posizione nel formato del HTML `<area>` dell’elemento [!DNL coords] attributo. Ad esempio: `coords ="0,0,84,128"`. |
| abilitato | `xsd:boolean` | True se la mappa immagine è abilitata. |
| lastModified | `xsd:dateTime` | Data e ora dell’ultima modifica apportata alla mappa immagine. |
