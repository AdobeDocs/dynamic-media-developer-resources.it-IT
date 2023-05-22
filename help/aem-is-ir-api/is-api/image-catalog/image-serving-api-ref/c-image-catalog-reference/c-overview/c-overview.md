---
description: I cataloghi di immagini vengono utilizzati per fornire al server informazioni sulle immagini e sui dati di supporto (come font e profili ICC).
solution: Experience Manager
title: Panoramica
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---

# Panoramica{#overview}

I cataloghi di immagini vengono utilizzati per fornire al server informazioni sulle immagini e sui dati di supporto (come font e profili ICC).

I cataloghi di immagini vengono utilizzati per fornire al server informazioni sulle immagini e sui dati di supporto (come font e profili ICC).

Ogni catalogo immagini è costituito da un file di attributi di catalogo obbligatorio e da un set di file di dati di catalogo facoltativi:

* Il file di dati immagine, che elenca in dettaglio immagini e modelli e i metadati associati.
* Il file di dati SVG, che elenca in dettaglio i file SVG e i metadati associati.
* Il file delle definizioni delle macro, che fornisce le definizioni per le macro di richiesta.
* Il file mappa dei caratteri, che tiene traccia dei caratteri di testo.
* Il file di mappa del profilo, che specifica i profili colore ICC.
* Il file del set di regole, che definisce le regole di pre-elaborazione delle richieste HTTP.

I file di dati del catalogo sono associati ai cataloghi di immagini tramite riferimenti di file nel file di attributi del catalogo. Lo stesso file di dati di catalogo può essere condiviso da più cataloghi di immagini.

I file degli attributi del catalogo devono avere [!DNL .ini] suffisso di file e deve trovarsi nel [!DNL Platform Server]Cartella del catalogo di ( `PlatformServer::catalog.rootPath`). I file di dati del catalogo possono trovarsi nella stessa cartella o in qualsiasi altra cartella accessibile al [!DNL Platform Server].

Questo documento descrive il formato di file del catalogo immagini per il sistema Dynamic Media Image Server. Il pubblico a cui si rivolge è costituito da programmatori esperti e sviluppatori di siti web che desiderano sfruttare Dynamic Media Image Server per un’applicazione web o personalizzata.

Si presume che il lettore abbia generalmente familiarità con il sistema Dynamic Media Image Server, gli standard e le convenzioni generali del protocollo HTTP e la terminologia di base dell’imaging.
