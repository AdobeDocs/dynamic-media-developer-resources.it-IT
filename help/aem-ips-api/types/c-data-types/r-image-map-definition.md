---
description: Definizione di destinazione per un’azione di clic nel browser.
seo-description: Definizione di destinazione per un’azione di clic nel browser.
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
topic: Scene7 Image Production System API
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 7%

---


# ImageMapDefinition{#imagemapdefinition}

Definizione di destinazione per un’azione di clic nel browser.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`name`*` | `xsd:string` | Nome della definizione della mappa immagine. |
| ` *`shapeType`*` | `xsd:string` | Uno dei valori di forma regione. |
| ` *`regione`*` | `xsd:string` | Coordinate mappa immagine. Il formato è basato sugli attributi di tag HTML `<area>`. |
| ` *`action`*` | `xsd:string` | Altri attributi da includere nel tag HTML `<area>`, incluso l&#39;URL `href`. |
| ` *`enabled`*` | `xsd:boolean` | True se la mappa immagine è abilitata. |

