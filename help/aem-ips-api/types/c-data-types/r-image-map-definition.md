---
description: Definizione di destinazione per un’azione di clic nel browser.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 8%

---

# ImageMapDefinition{#imagemapdefinition}

Definizione di destinazione per un’azione di clic nel browser.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| name | `xsd:string` | Nome della definizione della mappa immagine. |
| shapeType | `xsd:string` | Uno dei valori della forma regione. |
| regione | `xsd:string` | Coordinate mappa immagine. Il formato è basato su HTML `<area>` attributi del tag. |
| action | `xsd:string` | Altri attributi da includere in HTML `<area>` , compreso il `href` URL. |
| abilitato | `xsd:boolean` | True se la mappa immagine è abilitata. |
