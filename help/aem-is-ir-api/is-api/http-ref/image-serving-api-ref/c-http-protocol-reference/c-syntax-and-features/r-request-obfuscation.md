---
description: Il contenuto dell’intero modificatore parte della stringa di richiesta, incluso il suffisso di blocco facoltativo, può essere oscurato applicando la codifica standard base64.
seo-description: Il contenuto dell’intero modificatore parte della stringa di richiesta, incluso il suffisso di blocco facoltativo, può essere oscurato applicando la codifica standard base64.
seo-title: Oscuramento della richiesta
solution: Experience Manager
title: Oscuramento della richiesta
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 021c1d1f975083af3950775e230d4f73cbf9e0ec
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Oscuramento della richiesta{#request-obfuscation}

Il contenuto dell’intero modificatore parte della stringa di richiesta, incluso il suffisso di blocco facoltativo, può essere oscurato applicando la codifica standard base64.

Il server tenta di decodificare se `attribute::RequestObfuscation` è impostato. Se la decodifica non riesce, la richiesta viene rifiutata. Se sono applicati sia il blocco della richiesta che l&#39;oscuramento della richiesta, il suffisso del blocco deve essere generato e aggiunto prima della codifica base64.

>[!IMPORTANT]
>
>Se si abilita questa funzione, tenere presente che esistono alcune limitazioni all&#39;utilizzo che includono:<br>- L&#39;interfaccia utente di Dynamic Media potrebbe non mostrare i dettagli corretti per il campo **[!UICONTROL Last Published]**. Tuttavia, questo effetto non influisce sulla pubblicazione.<br>- Al momento, lo streaming video HLS non funziona quando **[!UICONTROL Richiedi]** oscuramento e  **[!UICONTROL Richiedi]** blocco sono abilitati.<br>- Al momento, alcuni visualizzatori Dynamic Media non funzionano quando  **[!UICONTROL Richiedi]** oscuramento e  **[!UICONTROL Richiedi]** blocco sono attivati.

## Esempio {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

codifica in:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Prima che la richiesta sia offuscata, è necessario che tutte le occorrenze di &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39; nelle stringhe dei valori siano precedute dalla codifica &#39;%xx&#39;. In caso contrario, non è necessario codificare http-encode la parte *modificatori* della richiesta prima o dopo l&#39;offuscamento, anche se viene applicato il blocco della richiesta, poiché la codifica base64 è sicura per la trasmissione http.

## Consultate anche {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Codifica](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7) HTTP,  [Blocco](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c) richieste,  [attributo::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
