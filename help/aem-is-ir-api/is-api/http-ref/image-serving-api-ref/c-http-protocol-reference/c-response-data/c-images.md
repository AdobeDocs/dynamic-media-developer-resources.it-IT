---
description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req=img o req=tmb.
seo-description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req=img o req=tmb.
seo-title: Immagini
solution: Experience Manager
title: Immagini
topic: Scene7 Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# Immagini{#images}

I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req=img o req=tmb.

Il tipo MIME di risposta HTTP è determinato da `fmt=`, oppure, se `fmt=` non è specificato, è `<image/jpeg>`.

Lo stato di risposta HTTP è &#39;200 OK&#39; se il metodo di richiesta era incondizionato `GET` o `HEAD`.

Il server può rispondere con stato &#39;304&#39; (non modificato) e non restituire dati immagine in risposta a una richiesta `GET` condizionale (che include un&#39;intestazione `If-Modified-Since` o `If-None-Match` valida).
