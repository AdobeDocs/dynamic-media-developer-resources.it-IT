---
description: Definizione di destinazione per un’azione di clic nel browser.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 5%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

Definizione di destinazione per un’azione di clic nel browser.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| nome | `xsd:string` | Nome della definizione della mappa immagine. |
| shapeType | `xsd:string` | Uno dei valori di forma dell&#39;area. |
| area geografica | `xsd:string` | Coordinate mappa immagine. Il formato si basa sulle HTML `<area>` attributi tag. |
| action | `xsd:string` | Altri attributi da includere nel HTML `<area>` , incluso `href` URL. |
| abilitato | `xsd:boolean` | True se la mappa immagine è attivata. |
