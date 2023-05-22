---
description: Questo è il registro principale che tiene traccia di tutte le richieste HTTP effettuate al [!DNL Platform Server]. Image Rendering, se attivato, scrive i dati del registro di accesso nello stesso file.
solution: Experience Manager
title: Registro di accesso
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Registro di accesso{#access-log}

Questo è il registro principale che tiene traccia di tutte le richieste HTTP effettuate al [!DNL Platform Server]. Image Rendering, se attivato, scrive i dati del registro di accesso nello stesso file.

Il registro di accesso è configurato in server.xml.

>[!NOTE]
>
>Oltre al traffico client per Image Server ( [!DNL /is/image/*]) e Image Rendering ( [!DNL /ir/render/*]), il registro di accesso può includere un certo traffico interno: l&#39;accesso al [!DNL Platform Server] sistema catalogo ( [!DNL /is-catalog/*]), condivisione della cache e richieste di reindirizzamento degli errori ( [!DNL /is/cache/*]), l&#39;accesso ad altri pacchetti distribuiti in [!DNL Platform Server], ad esempio i visualizzatori Dynamic Media ( [!DNL /is-viewers/*]), richieste di traffico statico e contenuti statici gestite da [!DNL Platform Server] (ad es. [!DNL /is-docs/*]).

Richieste con [!DNL /is-catalog] e [!DNL /is/cache] i percorsi radice devono sempre essere esclusi da qualsiasi analisi del traffico client.
