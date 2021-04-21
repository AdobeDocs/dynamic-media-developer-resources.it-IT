---
description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req=img o req=tmb.
solution: Experience Manager
title: Immagini
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 1%

---


# Immagini{#images}

I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req=img o req=tmb.

Il tipo MIME di risposta HTTP è determinato da `fmt=` oppure, se `fmt=` non è specificato, è `<image/jpeg>`.

Lo stato della risposta HTTP è &#39;200 OK&#39; se il metodo della richiesta era incondizionato `GET` o `HEAD`.

Il server può rispondere con lo stato &#39;304&#39; (non modificato) e non restituire alcun dato immagine in risposta a una richiesta condizionale `GET` (che include un&#39;intestazione valida `If-Modified-Since` o `If-None-Match`).
