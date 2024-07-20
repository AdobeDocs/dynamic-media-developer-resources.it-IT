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
ht-degree: 3%

---

# [!DNL ImageMap]{#imagemap}

Esegui il targeting per un’azione di clic nel browser.

Sempre associato a un&#39;immagine. È possibile ottenere una destinazione `ImageMap` da `ImageInfo`.

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| imageMapHandle | `xsd:string` | Handle mappa immagine. |
| [!DNL name] | `xsd:string` | Nome mappa immagine. |
| [!DNL region] | `xsd:string` | Coordinate mappa immagine. Il formato è basato sull&#39;attributo tag HTML `<area>`. |
| [!DNL action] | `xsd:string` | Altri attributi da includere nel tag HTML `<area>`, incluso l&#39;URL `href`. |
| shapeType | `xsd:boolean` | Un valore [!DNL RegionShape]. |
| [!DNL position] | `xsd:string` | Posizione nel formato dell&#39;attributo [!DNL coords] dell&#39;elemento HTML `<area>`. Esempio: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | True se la mappa immagine è abilitata. |
| lastModified | `xsd:dateTime` | Data e ora dell&#39;ultima modifica apportata alla mappa immagine. |
