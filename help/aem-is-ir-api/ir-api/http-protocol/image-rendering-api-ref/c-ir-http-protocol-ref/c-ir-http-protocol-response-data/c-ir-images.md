---
description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req= ha uno dei seguenti valori img, debug
seo-description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req= ha uno dei seguenti valori img, debug
seo-title: Immagini
solution: Experience Manager
title: Immagini
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 1%

---


# Immagini{#images}

I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req= ha uno dei seguenti valori: img, debug

Il tipo MIME di risposta HTTP è determinato da `fmt=` oppure, se `fmt=` non è specificato, dipende dal valore di `attribute::Format`.

Lo stato della risposta HTTP è &#39;200 OK&#39; se il metodo della richiesta era incondizionato `GET` o `HEAD`.

Il server può rispondere con lo stato &#39;304&#39; (non modificato) e non restituire dati immagine in risposta a una richiesta condizionale `GET` (con il campo [!DNL If-Modified-Since] presente in `request-header`).
