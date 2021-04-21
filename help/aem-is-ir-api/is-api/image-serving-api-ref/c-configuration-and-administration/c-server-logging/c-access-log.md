---
description: Si tratta del registro principale che tiene traccia di tutte le richieste HTTP effettuate al server Platform. Image Rendering, se abilitato, scrive i dati del registro di accesso nello stesso file.
solution: Experience Manager
title: Registro di accesso
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# Registro di accesso{#access-log}

Si tratta del registro principale che tiene traccia di tutte le richieste HTTP effettuate al server Platform. Image Rendering, se abilitato, scrive i dati del registro di accesso nello stesso file.

Il registro di accesso è configurato in server.xml.

>[!NOTE]
>
>Oltre al traffico client per Image Serving ( [!DNL /is/image/*]) e Image Rendering ( [!DNL /ir/render/*]), il registro di accesso può includere un determinato traffico interno: accesso al sistema di catalogo Platform Server ( [!DNL /is-catalog/*]), condivisione della cache e richieste di reindirizzamento degli errori ( [!DNL /is/cache/*]), accesso ad altri pacchetti implementati sul server Platform, come i visualizzatori Dynamic Media ( [!DNL /is-viewers/*]), richieste di traffico statico e di contenuto statico gestite dal server Platform (ad esempio [!DNL /is-docs/*]).

Le richieste con percorsi [!DNL /is-catalog] e [!DNL /is/cache] principali devono sempre essere escluse da qualsiasi analisi del traffico client.
