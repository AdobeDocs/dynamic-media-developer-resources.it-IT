---
description: I cataloghi di immagini vengono utilizzati per fornire informazioni sulle immagini e sui dati di supporto (come font e profili ICC) al server.
seo-description: I cataloghi di immagini vengono utilizzati per fornire informazioni sulle immagini e sui dati di supporto (come font e profili ICC) al server.
seo-title: Panoramica
solution: Experience Manager
title: Panoramica
topic: Scene7 Image Serving - Image Rendering API
uuid: e8c0401b-9161-4624-babb-6c7afb443e65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---


# Overview{#overview}

I cataloghi di immagini vengono utilizzati per fornire informazioni sulle immagini e sui dati di supporto (come font e profili ICC) al server.

I cataloghi di immagini vengono utilizzati per fornire informazioni sulle immagini e sui dati di supporto (come font e profili ICC) al server.

Ciascun catalogo di immagini è costituito da un file attributo di catalogo obbligatorio e da un set di file di dati di catalogo opzionali:

* Il file di dati immagine, che riassume le immagini e i modelli e i relativi metadati.
* Il file di dati SVG, che riproduce i file SVG e i metadati associati.
* Il file delle definizioni delle macro, che fornisce le definizioni per le macro delle richieste.
* Il file della mappa dei font, che tiene traccia dei font di testo.
* Il file della mappa del profilo, che rappresenta i profili colore ICC.
* Il file set di regole, che definisce le regole di pre-elaborazione delle richieste HTTP.

I file di dati del catalogo sono associati ai cataloghi di immagini in base ai riferimenti ai file presenti nel file di attributi del catalogo. Lo stesso file di dati del catalogo può essere condiviso da più cataloghi di immagini.

I file di attributi del catalogo devono avere un suffisso di file [!DNL .ini] e devono trovarsi nella cartella del catalogo del server piattaforme ( `PlatformServer::catalog.rootPath`). I file di dati del catalogo possono trovarsi nella stessa cartella o in qualsiasi altra cartella accessibile al server della piattaforma.

Questo documento descrive il formato del file catalogo immagini per il sistema Scene7 Image Server. L&#39;audience prevista è composta da programmatori esperti e sviluppatori di siti Web che desiderano sfruttare Scene7 Image Server per un&#39;applicazione Web o personalizzata.

Si presume che il lettore abbia familiarità con il sistema Scene7 Image Server, con gli standard e le convenzioni generali del protocollo HTTP e con la terminologia di base per l’imaging.
