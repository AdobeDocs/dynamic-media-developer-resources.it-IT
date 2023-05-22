---
description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= oppure req=img o req=tmb.
solution: Experience Manager
title: Immagini
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 1%

---

# Immagini{#images}

I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= oppure req=img o req=tmb.

Il tipo MIME di risposta HTTP è determinato da `fmt=`, o, se `fmt=` non è specificato, è `<image/jpeg>`.

Lo stato della risposta HTTP è &quot;200 OK&quot; se il metodo di richiesta era incondizionato `GET` o `HEAD`.

Il server può rispondere con lo stato &#39;304&#39; (non modificato) e non restituire dati immagine in risposta a un condizionale `GET` richiesta (che include un `If-Modified-Since` o `If-None-Match` header).
