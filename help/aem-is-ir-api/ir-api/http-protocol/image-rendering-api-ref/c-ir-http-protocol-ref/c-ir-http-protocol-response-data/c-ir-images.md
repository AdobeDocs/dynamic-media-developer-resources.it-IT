---
description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req=, oppure se req= ha uno dei seguenti valori img, debug
seo-description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req=, oppure se req= ha uno dei seguenti valori img, debug
seo-title: Immagini
solution: Experience Manager
title: Immagini
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---


# Immagini{#images}

I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req= ha uno dei seguenti valori: img, debug

Il tipo MIME di risposta HTTP è determinato da `fmt=`, oppure, se `fmt=` non è specificato, dipende dal valore di `attribute::Format`.

Lo stato di risposta HTTP è &#39;200 OK&#39; se il metodo di richiesta era incondizionato `GET` o `HEAD`.

Il server può rispondere con stato &#39;304&#39; (non modificato) e non restituire dati immagine in risposta a una richiesta `GET` condizionale (con il campo [!DNL If-Modified-Since] presente in `request-header`).
