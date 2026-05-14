---
description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= oppure req=img o req=tmb.
solution: Experience Manager
title: Immagini
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
TQID: 'https://experienceleague.adobe.com/1tStTbuCLrOG8XrPgOw5qH-VujpHXX8Pt0IWXg9329Y'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 1%

---

# Immagini{#images}

I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= oppure req=img o req=tmb.

Il tipo MIME di risposta HTTP è determinato da `fmt=` oppure, se `fmt=` non è specificato, è `<image/jpeg>`.

Lo stato della risposta HTTP è &#39;200 OK&#39; se il metodo di richiesta era `GET` o `HEAD` incondizionato.

Il server potrebbe rispondere con lo stato &#39;304&#39; (non modificato) e non restituire alcun dato immagine in risposta a una richiesta condizionale `GET` (che include un&#39;intestazione `If-Modified-Since` o `If-None-Match` valida).
