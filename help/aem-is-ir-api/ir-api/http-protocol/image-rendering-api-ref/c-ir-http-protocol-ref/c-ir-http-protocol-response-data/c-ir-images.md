---
title: Immagini
description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req= ha uno dei seguenti valori img, debug.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 1%

---

# Immagini{#images}

I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= o se req= ha uno dei seguenti valori: img, debug

Il tipo MIME di risposta HTTP è determinato da `fmt=`o, se `fmt=` non è specificato, dipende dal valore di `attribute::Format`.

Lo stato di risposta HTTP è &#39;200 OK&#39; se il metodo di richiesta era incondizionato `GET` o `HEAD`.

Il server può rispondere con lo stato &#39;304&#39; (non modificato) e non restituire alcun dato immagine in risposta a un `GET` (con [!DNL If-Modified-Since] campo presente `request-header`).
