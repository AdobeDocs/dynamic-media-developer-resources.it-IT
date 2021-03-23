---
description: I valori dei comandi devono essere codificati in http utilizzando %xx sequenze di escape, in modo che le stringhe di valori non includano i caratteri riservati '=', '&' e '%'.
seo-description: I valori dei comandi devono essere codificati in http utilizzando %xx sequenze di escape, in modo che le stringhe di valori non includano i caratteri riservati '=', '&' e '%'.
seo-title: Codifica HTTP del rendering delle immagini
solution: Experience Manager
title: Codifica HTTP del rendering delle immagini
uuid: 37bd0040-7bad-4548-ab39-7f598a217732
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 1%

---


# Image Rendering HTTP encoding{#image-rendering-http-encoding}

I valori dei comandi devono essere codificati in http utilizzando %xx sequenze di escape, in modo che le stringhe di valori non includano i caratteri riservati &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39;.

In caso contrario, si applicano le regole di codifica HTTP standard. La specifica HTTP richiede la codifica dei caratteri non sicuri come &#39; &#39; (spazio), &#39;&#39;(virgolette doppie), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; e &#39;>&#39;, nonché di tutti i caratteri di controllo, come `<return>` e `<tab>`.

**Attenzione:** le parentesi graffe { } utilizzate come delimitatori di nidificazione delle richieste non devono essere codificate. Alcuni client di posta elettronica codificano purtroppo le parentesi graffe nella richiesta HTTP incorporata. In caso di problemi, Image Rendering consente l’uso di parentesi tonde ( ) invece di parentesi graffe.

## Esempio {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Il frammento di richiesta di cui sopra deve essere codificato come segue:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Consultate anche {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[Specifiche HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
