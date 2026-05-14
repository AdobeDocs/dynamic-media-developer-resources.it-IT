---
title: Immagini
description: I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= oppure se req= ha uno dei seguenti valori img, debug.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
TQID: 'https://experienceleague.adobe.com/4wHyyXX0gxz9ojr5g5Puu5fBhKXo4hZDjyBuVTao3rQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 1%

---

# Immagini{#images}

I dati immagine vengono restituiti se una richiesta viene completata correttamente e se la richiesta non include un comando req= oppure se req= ha uno dei seguenti valori: img, debug

Il tipo MIME di risposta HTTP è determinato da `fmt=` oppure, se `fmt=` non è specificato, dipende dal valore di `attribute::Format`.

Lo stato della risposta HTTP è &#39;200 OK&#39; se il metodo di richiesta era `GET` o `HEAD` incondizionato.

Il server potrebbe rispondere con lo stato &#39;304&#39; (non modificato) e non restituire alcun dato immagine in risposta a una richiesta condizionale `GET` (con il campo [!DNL If-Modified-Since] presente in `request-header`).
