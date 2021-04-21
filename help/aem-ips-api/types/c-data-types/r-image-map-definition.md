---
description: Definizione di destinazione per un’azione di clic nel browser.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
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

