---
description: Si tratta del registro principale che tiene traccia di tutte le richieste HTTP effettuate al server Platform. Image Rendering, se abilitato, scrive i dati del registro di accesso nello stesso file.
solution: Experience Manager
title: Registro di accesso
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Registro di accesso{#access-log}

Si tratta del registro principale che tiene traccia di tutte le richieste HTTP effettuate al server Platform. Image Rendering, se abilitato, scrive i dati del registro di accesso nello stesso file.

Il registro di accesso è configurato in server.xml.

>[!NOTE]
>
>Oltre al traffico client per Image Serving ( [!DNL /is/image/*]) e Image Rendering ( [!DNL /ir/render/*]), il registro di accesso può includere un determinato traffico interno: accesso al sistema di catalogo Platform Server ( [!DNL /is-catalog/*]), condivisione della cache e richieste di reindirizzamento degli errori ( [!DNL /is/cache/*]), accesso ad altri pacchetti implementati sul server Platform, come i visualizzatori Dynamic Media ( [!DNL /is-viewers/*]), richieste di traffico statico e di contenuto statico gestite dal server Platform (ad esempio [!DNL /is-docs/*]).

Le richieste con percorsi [!DNL /is-catalog] e [!DNL /is/cache] principali devono sempre essere escluse da qualsiasi analisi del traffico client.
