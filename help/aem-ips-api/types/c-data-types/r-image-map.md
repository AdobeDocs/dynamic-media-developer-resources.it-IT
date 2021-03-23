---
description: Individua un’azione di clic nel browser.
seo-description: Individua un’azione di clic nel browser.
seo-title: Mappa immagine
solution: Experience Manager
title: Mappa immagine
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 10%

---


# Mappa immagine{#imagemap}

Individua un’azione di clic nel browser.

Sempre associata a un&#39;immagine. Puoi ottenere una destinazione `ImageMap` da `ImageInfo`.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | Maniglia mappa immagine. |
| `*`name`*` | `xsd:string` | Nome mappa immagine. |
| `*`regione`*` | `xsd:string` | Coordinate mappa immagine. Il formato è basato sull&#39;attributo tag HTML `<area>` . |
| `*`action`*` | `xsd:string` | Altri attributi da includere nel tag HTML `<area>`, incluso l’ `href` URL. |
| `*`shapeType`*` | `xsd:boolean` | Valore [!DNL RegionShape]. |
| `*`position`*` | `xsd:string` | Posizione nel formato dell’attributo dell’elemento HTML `<area>` [!DNL coords] . Ad esempio: `coords ="0,0,84,128"`. |
| `*`abilitato`*` | `xsd:boolean` | True se la mappa immagine è abilitata. |
| `*`lastModified`*` | `xsd:dateTime` | Data e ora dell’ultima modifica apportata alla mappa immagine. |

