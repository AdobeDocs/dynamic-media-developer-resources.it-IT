---
description: Si tratta del registro principale che tiene traccia di tutte le richieste HTTP effettuate al server piattaforma. Il rendering delle immagini, se attivato, scrive i dati del registro di accesso nello stesso file.
seo-description: Si tratta del registro principale che tiene traccia di tutte le richieste HTTP effettuate al server piattaforma. Il rendering delle immagini, se attivato, scrive i dati del registro di accesso nello stesso file.
seo-title: Registro di accesso
solution: Experience Manager
title: Registro di accesso
topic: Scene7 Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Registro di accesso{#access-log}

Si tratta del registro principale che tiene traccia di tutte le richieste HTTP effettuate al server piattaforma. Il rendering delle immagini, se attivato, scrive i dati del registro di accesso nello stesso file.

Il registro di accesso è configurato in server.xml.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Oltre al traffico client per Image Server ( [!DNL /is/image/*]) e Image Rendering ( [!DNL /ir/render/*]), il registro di accesso può includere anche un determinato traffico interno: accesso al sistema di cataloghi Platform Server ( [!DNL /is-catalog/*]), condivisione della cache e richieste di reindirizzamento degli errori ( [!DNL /is/cache/*]), accesso ad altri pacchetti distribuiti sul server piattaforme, come i visualizzatori Scene7 ( [!DNL /is-viewers/*]), richieste di traffico statico e di contenuto statico servite dal server piattaforme (ad esempio [!DNL /is-docs/*]).

Le richieste con [!DNL /is-catalog] e i percorsi [!DNL /is/cache] principali devono essere sempre escluse dall&#39;analisi del traffico client.
