---
title: Codifica HTTP del rendering delle immagini
description: I valori dei comandi devono essere codificati in http utilizzando %xx sequenze di escape, in modo che le stringhe di valori non includano i caratteri riservati '=', '&' e '%'.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---

# Codifica HTTP del rendering delle immagini{#image-rendering-http-encoding}

I valori dei comandi devono essere codificati in http utilizzando %xx sequenze di escape, in modo che le stringhe di valori non includano i caratteri riservati &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39;.

In caso contrario, si applicano le regole di codifica HTTP standard. La specifica HTTP richiede la codifica dei caratteri non sicuri come &#39; (spazio), &#39;&quot; (virgolette doppie), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; e &#39;>&#39;, nonché di eventuali caratteri di controllo, ad esempio `<return>` e `<tab>`.

**Attenzione:** Le parentesi graffe { } utilizzate come delimitatori di nidificazione delle richieste non devono essere codificate. Alcuni client di posta elettronica codificano purtroppo le parentesi graffe nella richiesta HTTP incorporata. Se questo problema si verifica, Image Rendering consente l’uso di parentesi tonde ( ) invece di parentesi graffe.

## Esempio {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Il frammento di richiesta di cui sopra deve essere codificato come segue:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Consultate anche {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[Specifiche HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
