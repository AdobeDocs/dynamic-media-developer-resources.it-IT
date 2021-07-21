---
description: Definizione di destinazione per un’azione di clic nel browser.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 7%

---

# ImageMapDefinition{#imagemapdefinition}

Definizione di destinazione per un’azione di clic nel browser.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`name`*` | `xsd:string` | Nome della definizione della mappa immagine. |
| `*`shapeType`*` | `xsd:string` | Uno dei valori della forma regione. |
| `*`regione`*` | `xsd:string` | Coordinate mappa immagine. Il formato è basato sugli attributi del tag HTML `<area>` . |
| `*`action`*` | `xsd:string` | Altri attributi da includere nel tag HTML `<area>`, incluso l’ `href` URL. |
| `*`abilitato`*` | `xsd:boolean` | True se la mappa immagine è abilitata. |
