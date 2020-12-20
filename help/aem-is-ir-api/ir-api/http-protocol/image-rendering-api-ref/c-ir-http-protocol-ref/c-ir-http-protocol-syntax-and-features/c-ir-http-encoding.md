---
description: I valori dei comandi devono essere codificati http-encoded utilizzando %xx sequenze di escape, in modo che le stringhe dei valori non includano i caratteri riservati '=', '&' e '%'.
seo-description: I valori dei comandi devono essere codificati http-encoded utilizzando %xx sequenze di escape, in modo che le stringhe dei valori non includano i caratteri riservati '=', '&' e '%'.
seo-title: Image Rendering HTTP encoding
solution: Experience Manager
title: Image Rendering HTTP encoding
topic: Scene7 Image Serving - Image Rendering API
uuid: 37bd0040-7bad-4548-ab39-7f598a217732
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# Image Rendering HTTP encoding{#image-rendering-http-encoding}

I valori dei comandi devono essere codificati http-encoded utilizzando %xx sequenze di escape, in modo che le stringhe dei valori non includano i caratteri riservati &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39;.

In caso contrario, si applicano le regole di codifica HTTP standard. La specifica HTTP richiede la codifica dei caratteri non sicuri come &#39; (spazio), &#39;&quot;(virgolette doppie), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; e &#39;>&#39;, nonché di tutti i caratteri di controllo, come `<return>` e `<tab>`.

**Attenzione:** le parentesi graffe { } utilizzate come delimitatori di nidificazione delle richieste non devono essere codificate. Alcuni client e-mail codificano purtroppo le parentesi graffe nella richiesta HTTP incorporata. Se si verifica questo problema, Image Rendering consente l’uso delle parentesi ( ) invece delle parentesi graffe.

## Esempio {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Il frammento di richiesta di cui sopra deve essere codificato come segue:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Consultate anche {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[Specifica HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
