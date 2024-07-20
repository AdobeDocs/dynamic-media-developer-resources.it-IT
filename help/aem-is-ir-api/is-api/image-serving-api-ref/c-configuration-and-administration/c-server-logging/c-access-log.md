---
description: Questo è il registro primario che tiene traccia di tutte le richieste HTTP effettuate a  [!DNL Platform Server]. Image Rendering, se attivato, scrive i dati del registro di accesso nello stesso file.
solution: Experience Manager
title: Registro di accesso
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Registro di accesso{#access-log}

Questo è il registro primario che tiene traccia di tutte le richieste HTTP effettuate a [!DNL Platform Server]. Image Rendering, se attivato, scrive i dati del registro di accesso nello stesso file.

Il registro di accesso è configurato in server.xml.

>[!NOTE]
>
>Oltre al traffico client per Image Server ( [!DNL /is/image/*]) e Image Rendering ( [!DNL /ir/render/*]), il log degli accessi può includere un certo traffico interno: accesso al sistema di catalogo [!DNL Platform Server] ( [!DNL /is-catalog/*]), condivisione cache e richieste di reindirizzamento degli errori ( [!DNL /is/cache/*]), accesso ad altri pacchetti distribuiti in [!DNL Platform Server], ad esempio visualizzatori Dynamic Medie ( [!DNL /is-viewers/*]), traffico statico e richieste di contenuto statico gestite da [!DNL Platform Server] (ad esempio [!DNL /is-docs/*]).

Le richieste con [!DNL /is-catalog] e [!DNL /is/cache] percorsi principali devono sempre essere escluse dall&#39;analisi del traffico client.
