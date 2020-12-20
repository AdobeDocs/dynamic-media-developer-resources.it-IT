---
description: Image Server supporta l’accesso alle immagini sorgente su server HTTP e FTP esterni.
seo-description: Image Server supporta l’accesso alle immagini sorgente su server HTTP e FTP esterni.
seo-title: Origini immagine straniere
solution: Experience Manager
title: Origini immagine straniere
topic: Scene7 Image Serving - Image Rendering API
uuid: 28a17400-4807-4e14-937a-80309be53d55
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Origini immagine straniere{#foreign-image-sources}

Image Server supporta l’accesso alle immagini sorgente su server HTTP e FTP esterni.

Per specificare un URL esterno per un comando `src=` o `mask=`; delimitate semplicemente l’intero URL incorporato con parentesi graffe:

` …&src={ *[!DNL foreignUrl]*}&…`

Sono consentiti URL assoluti completi (se è impostato `attribute::AllowDirectUrls`) e URL relativi a `attribute::RootUrl`. Si verifica un errore se un URL assoluto è incorporato e attributo: `AllowDirectUrls` è 0 oppure se è specificato un URL relativo e `attribute::RootUrl` è vuoto.

Le immagini esterne vengono memorizzate nella cache dal server in base alle intestazioni di cache incluse nella risposta HTTP.
