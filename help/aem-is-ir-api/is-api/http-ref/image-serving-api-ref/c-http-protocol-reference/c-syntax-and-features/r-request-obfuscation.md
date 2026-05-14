---
description: Il contenuto dell’intera parte dei modificatori della stringa di richiesta, incluso il suffisso di blocco opzionale, può essere oscurato applicando la codifica standard base64.
solution: Experience Manager
title: Richiedi offuscamento
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
TQID: 'https://experienceleague.adobe.com/77Q5rV3cP4KoBz3rFKlEmBlumS0TBthuLbLQBETPitE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 1%

---

# Richiedi offuscamento{#request-obfuscation}

Il contenuto dell’intera parte dei modificatori della stringa di richiesta, incluso il suffisso di blocco opzionale, può essere oscurato applicando la codifica standard base64.

Il server tenta di decodificare se `attribute::RequestObfuscation` è impostato. Se la decodifica non riesce, la richiesta viene rifiutata. Se vengono applicati sia il blocco delle richieste che l’offuscamento delle richieste, il suffisso di blocco deve essere generato e aggiunto prima della codifica base64.

>[!IMPORTANT]
>
>Se abiliti questa funzione, tieni presente che esistono alcune limitazioni al suo utilizzo che includono quanto segue:<br>- L&#39;interfaccia utente di Dynamic Media potrebbe non mostrare i dettagli corretti per il campo **[!UICONTROL Ultima pubblicazione]**. Tuttavia, questo effetto non influisce sulla pubblicazione.<br>- Attualmente, il flusso video HLS non funziona quando **[!UICONTROL Offuscamento richiesta]** e **[!UICONTROL Blocco richiesta]** sono abilitati.<br>- Attualmente, alcuni visualizzatori Dynamic Media non funzionano quando **[!UICONTROL Offuscamento richiesta]** e **[!UICONTROL Blocco richiesta]** sono abilitati.

## Esempio {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

codifica in:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Eventuali occorrenze di &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39; nelle stringhe di valore devono essere precedute dalla sequenza di escape utilizzando la codifica &#39;%xx&#39;, prima che la richiesta venga offuscata. In caso contrario, non è necessario codificare http la parte *modificatori* della richiesta prima o dopo l&#39;offuscamento, anche se viene applicato il blocco della richiesta, poiché la codifica base64 è sicura per la trasmissione http.

## Consultate anche {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[Codifica HTTP](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Blocco richieste](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [attributo::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
