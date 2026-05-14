---
description: Questo è il registro primario che tiene traccia di tutte le richieste HTTP effettuate a  [!DNL Platform Server]. Image Rendering, se attivato, scrive i dati del registro di accesso nello stesso file.
solution: Experience Manager
title: Registro di accesso
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
TQID: 'https://experienceleague.adobe.com/PXdlJ0gBGbq4FFhoG6gtmG3hrWVWsXIPelL9xXy5ESk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 0%

---

# Registro di accesso{#access-log}

Questo è il registro primario che tiene traccia di tutte le richieste HTTP effettuate a [!DNL Platform Server]. Image Rendering, se attivato, scrive i dati del registro di accesso nello stesso file.

Il registro di accesso è configurato in server.xml.

>[!NOTE]
>
>Oltre al traffico client per Image Server ( [!DNL /is/image/*]) e Image Rendering ( [!DNL /ir/render/*]), il log degli accessi può includere un certo traffico interno: accesso al sistema di catalogo [!DNL Platform Server] ( [!DNL /is-catalog/*]), condivisione cache e richieste di reindirizzamento degli errori ( [!DNL /is/cache/*]), accesso ad altri pacchetti distribuiti in [!DNL Platform Server], ad esempio visualizzatori Dynamic Media ( [!DNL /is-viewers/*]), traffico statico e richieste di contenuto statico gestite da [!DNL Platform Server] (ad esempio [!DNL /is-docs/*]).

Le richieste con [!DNL /is-catalog] e [!DNL /is/cache] percorsi principali devono sempre essere escluse dall&#39;analisi del traffico client.
