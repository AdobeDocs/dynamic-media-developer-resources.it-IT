---
description: Il contenuto dell’intera parte dei modificatori della stringa di richiesta, incluso il suffisso di blocco opzionale, può essere oscurato applicando la codifica standard base64.
solution: Experience Manager
title: Richiedi offuscamento
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 1%

---

# Richiedi offuscamento{#request-obfuscation}

Il contenuto dell’intera parte dei modificatori della stringa di richiesta, incluso il suffisso di blocco opzionale, può essere oscurato applicando la codifica standard base64.

Il server tenta di decodificare se `attribute::RequestObfuscation` è impostato. Se la decodifica non riesce, la richiesta viene rifiutata. Se vengono applicati sia il blocco delle richieste che l’offuscamento delle richieste, il suffisso di blocco deve essere generato e aggiunto prima della codifica base64.

>[!IMPORTANT]
>
>Se abiliti questa funzione, tieni presente che l’utilizzo di essa è soggetto a determinate limitazioni, tra cui:<br>- L&#39;interfaccia utente di Dynamic Media potrebbe non mostrare i dettagli corretti per **[!UICONTROL Ultima pubblicazione]** campo. Tuttavia, questo effetto non influisce sulla pubblicazione.<br>- Attualmente, lo streaming video HLS non funziona quando **[!UICONTROL Richiedi offuscamento]** e **[!UICONTROL Richiedi blocco]** sono attivati.<br>- Attualmente, alcuni visualizzatori Dynamic Media non funzionano quando **[!UICONTROL Richiedi offuscamento]** e **[!UICONTROL Richiedi blocco]** sono attivati.

## Esempio {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

codifica in:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Eventuali occorrenze di &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39; nelle stringhe di valore devono essere precedute dalla sequenza di escape utilizzando la codifica &#39;%xx&#39;, prima che la richiesta venga offuscata. Non è necessario codificare altrimenti http il *modificatori* parte della richiesta prima o dopo l’offuscamento, anche se viene applicato il blocco della richiesta, in quanto la codifica base64 è sicura per la trasmissione http.

## Consultate anche {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Codifica HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Richiedi blocco](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [attribute::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
