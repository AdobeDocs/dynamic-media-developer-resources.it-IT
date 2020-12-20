---
description: Eseguire il targeting per un'azione di clic nel browser.
seo-description: Eseguire il targeting per un'azione di clic nel browser.
seo-title: Mappa immagine
solution: Experience Manager
title: Mappa immagine
topic: Scene7 Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 11%

---


# Mappa immagine{#imagemap}

Eseguire il targeting per un&#39;azione di clic nel browser.

Sempre associata a un’immagine. È possibile ottenere una destinazione `ImageMap` da `ImageInfo`.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | Maniglia della mappa immagine. |
| ` *`name`*` | `xsd:string` | Nome mappa immagine. |
| ` *`regione`*` | `xsd:string` | Coordinate mappa immagine. Il formato è basato sull&#39;attributo di tag HTML `<area>`. |
| ` *`action`*` | `xsd:string` | Altri attributi da includere nel tag HTML `<area>`, incluso l&#39;URL `href`. |
| ` *`shapeType`*` | `xsd:boolean` | Un valore [!DNL RegionShape]. |
| ` *`position`*` | `xsd:string` | Posizione nel formato dell&#39;attributo `<area>` dell&#39;elemento HTML [!DNL coords]. Ad esempio: `coords ="0,0,84,128"`. |
| ` *`enabled`*` | `xsd:boolean` | True se la mappa immagine è abilitata. |
| ` *`lastModified`*` | `xsd:dateTime` | Data e ora dell’ultima modifica della mappa immagine. |

