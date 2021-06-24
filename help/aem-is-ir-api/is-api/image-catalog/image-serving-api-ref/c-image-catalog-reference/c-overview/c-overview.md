---
description: I cataloghi di immagini vengono utilizzati per fornire informazioni sulle immagini e sui dati di supporto (come font e profili ICC) al server.
solution: Experience Manager
title: Panoramica
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Panoramica{#overview}

I cataloghi di immagini vengono utilizzati per fornire informazioni sulle immagini e sui dati di supporto (come font e profili ICC) al server.

I cataloghi di immagini vengono utilizzati per fornire informazioni sulle immagini e sui dati di supporto (come font e profili ICC) al server.

Ogni catalogo di immagini è costituito da un file di attributi di catalogo richiesto e da un set di file di dati di catalogo opzionali:

* Il file di dati immagine, che riprende le immagini e i modelli e i metadati associati.
* Il file di dati SVG, che descrive i file SVG e i relativi metadati associati.
* Il file delle definizioni delle macro, che fornisce le definizioni delle macro delle richieste.
* Il file di mappa dei font, che tiene traccia dei font di testo.
* Il file di mappa del profilo, che descrive i profili di colore ICC.
* Il file set di regole, che definisce le regole di pre-elaborazione delle richieste HTTP.

I file di dati del catalogo sono associati ai cataloghi di immagini mediante riferimenti di file nel file di attributi del catalogo. Lo stesso file di dati di catalogo può essere condiviso da più cataloghi di immagini.

I file di attributi del catalogo devono avere un suffisso di file [!DNL .ini] e devono trovarsi nella cartella del catalogo di Platform Server ( `PlatformServer::catalog.rootPath`). I file di dati del catalogo possono trovarsi nella stessa cartella o in qualsiasi altra cartella accessibile al server Platform.

Questo documento descrive il formato del file del catalogo immagini per il sistema Image Serving di Dynamic Media. Il pubblico a cui è destinato è composto da programmatori esperti e sviluppatori di siti web che desiderano sfruttare Dynamic Media Image Serving per un&#39;applicazione web o personalizzata.

Si presume che il lettore abbia generalmente familiarità con il sistema Image Serving di Dynamic Media, gli standard e le convenzioni generali del protocollo HTTP e la terminologia di imaging di base.
