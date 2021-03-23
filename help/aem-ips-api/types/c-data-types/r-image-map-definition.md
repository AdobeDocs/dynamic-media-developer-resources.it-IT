---
description: Definizione di destinazione per un’azione di clic nel browser.
seo-description: Definizione di destinazione per un’azione di clic nel browser.
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 6%

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

