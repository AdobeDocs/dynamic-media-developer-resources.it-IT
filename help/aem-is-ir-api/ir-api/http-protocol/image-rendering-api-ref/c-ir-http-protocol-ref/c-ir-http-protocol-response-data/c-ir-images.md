---
description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req=, oppure se req= ha uno dei seguenti valori img, debug
seo-description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req=, oppure se req= ha uno dei seguenti valori img, debug
seo-title: Immagini
solution: Experience Manager
title: Immagini
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Immagini{#images}

I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req= ha uno dei seguenti valori: img, debug

Il tipo MIME di risposta HTTP è determinato dal `fmt=`valore di `fmt=` , oppure, se non `attribute::Format`è specificato, dipende da esso.

Lo stato di risposta HTTP è &#39;200 OK&#39; se il metodo di richiesta era incondizionato `GET` o `HEAD`.

Il server può rispondere con lo stato &#39;304&#39; (non modificato) e non restituire alcun dato immagine in risposta a una `GET` richiesta condizionale (con il [!DNL If-Modified-Since] campo presente nel `request-header`).
