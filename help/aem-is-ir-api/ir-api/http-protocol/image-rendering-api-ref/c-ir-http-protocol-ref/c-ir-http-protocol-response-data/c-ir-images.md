---
description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req= ha uno dei seguenti valori img, debug.
solution: Experience Manager
title: Immagini
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---

# Immagini{#images}

I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req= ha uno dei seguenti valori: img, debug

Il tipo MIME di risposta HTTP è determinato da `fmt=` oppure, se `fmt=` non è specificato, dipende dal valore di `attribute::Format`.

Lo stato della risposta HTTP è &#39;200 OK&#39; se il metodo della richiesta era incondizionato `GET` o `HEAD`.

Il server può rispondere con lo stato &#39;304&#39; (non modificato) e non restituire dati immagine in risposta a una richiesta condizionale `GET` (con il campo [!DNL If-Modified-Since] presente in `request-header`).
