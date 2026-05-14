---
description: I cataloghi di immagini vengono utilizzati per fornire al server informazioni sulle immagini e sui dati di supporto (come font e profili ICC).
solution: Experience Manager
title: Panoramica
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36cdd833-6fcb-4be6-a4f8-ba8d20580f29
TQID: 'https://experienceleague.adobe.com/RFHaFaMFjOo2Igk-pQRXrQSCtSMmVCWarO6wu0mv4g8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# Panoramica{#overview}

I cataloghi di immagini vengono utilizzati per fornire al server informazioni sulle immagini e sui dati di supporto (come font e profili ICC).

I cataloghi di immagini vengono utilizzati per fornire al server informazioni sulle immagini e sui dati di supporto (come font e profili ICC).

Ogni catalogo immagini è costituito da un file di attributi di catalogo obbligatorio e da un set di file di dati di catalogo facoltativi:

* Il file di dati immagine, che elenca in dettaglio immagini e modelli e i metadati associati.
* Il file di dati SVG, che descrive dettagliatamente i file SVG e i metadati associati.
* Il file delle definizioni delle macro, che fornisce le definizioni per le macro di richiesta.
* Il file mappa dei caratteri, che tiene traccia dei caratteri di testo.
* Il file di mappa del profilo, che specifica i profili colore ICC.
* Il file del set di regole, che definisce le regole di pre-elaborazione delle richieste HTTP.

I file di dati del catalogo sono associati ai cataloghi di immagini tramite riferimenti di file nel file di attributi del catalogo. Lo stesso file di dati di catalogo può essere condiviso da più cataloghi di immagini.

I file degli attributi del catalogo devono avere un suffisso di file [!DNL .ini] e devono trovarsi nella cartella del catalogo di [!DNL Platform Server] ( `PlatformServer::catalog.rootPath`). I file di dati del catalogo possono trovarsi nella stessa cartella o in qualsiasi altra cartella accessibile a [!DNL Platform Server].

Questo documento descrive il formato di file del catalogo immagini per il sistema Dynamic Media Image Server. Il pubblico a cui si rivolge è composto da programmatori esperti e sviluppatori di siti web che desiderano sfruttare Dynamic Media Image Server per un’applicazione web o personalizzata.

Si presume che il lettore abbia generalmente familiarità con il sistema Dynamic Media Image Server, gli standard e le convenzioni generali del protocollo HTTP e la terminologia di base dell’imaging.
