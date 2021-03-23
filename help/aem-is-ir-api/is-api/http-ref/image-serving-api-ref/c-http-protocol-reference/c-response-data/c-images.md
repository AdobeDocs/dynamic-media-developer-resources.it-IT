---
description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req=img o req=tmb.
seo-description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req=img o req=tmb.
seo-title: Immagini
solution: Experience Manager
title: Immagini
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---


# Immagini{#images}

I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req=img o req=tmb.

Il tipo MIME di risposta HTTP è determinato da `fmt=` oppure, se `fmt=` non è specificato, è `<image/jpeg>`.

Lo stato della risposta HTTP è &#39;200 OK&#39; se il metodo della richiesta era incondizionato `GET` o `HEAD`.

Il server può rispondere con lo stato &#39;304&#39; (non modificato) e non restituire alcun dato immagine in risposta a una richiesta condizionale `GET` (che include un&#39;intestazione valida `If-Modified-Since` o `If-None-Match`).
